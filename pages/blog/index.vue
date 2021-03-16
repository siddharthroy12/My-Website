<template>
  <div class="_container">
    <div class="content">
      <div class="header">
        <h1>Blog</h1>
        <h3>
          {{ description }}
        </h3>
      </div>
      <div class="blog-list">
        <BlogCard v-for="(blog, index) in blogs" :key="index"
          :banner="blog.banner"
          :title="blog.title"
          :desc="stripContent(blog)"
          :slug="blog.slug"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      titleTemplate: '%s - Blog',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.description
        }
      ]
    }
  },

  data() {
    return {
      description:
        'So every dev has one problem we tend forget how we did something but ' +
        'I found a solution and you are looking right at it. Yes!! This blog is my solution ' +
        'So welcome and I hope you find what you came looking for.',
      blogs: []
    }
  },

  methods: {
    getText(element) {
      if (element.type === 'text') {
        return element.value
      }

      let res = ""

      for(let i = 0; i < element.children.length; i++) {
        res += this.getText(element.children[i])
      }

      return res
    },

    stripContent(blog) {
      let someContent = ""
      for(let i = 0; i < 5 || i < blog.body.children.length; i++) {
        someContent += this.getText(blog.body.children[i])
      }
      return someContent.slice(0, 200) + '...'
    },
  },

  async fetch() {
		const blogs = await this.$content('blogs').fetch()
		this.blogs = blogs
	}
}
</script>

<style scoped>
._container {
  display: flex;
  justify-content: center;
}

.content {
  width: 100%;
  max-width: 50rem;
}

.header {
  padding: 0 2rem;
}

h1 {
  font-size: 3rem;
  font-weight: 600;
  border-bottom: 1px solid #D3D3D3;
  width: fit-content;
  margin: 3rem 0;
}

h3 {
  font-size: 1.125rem;
  line-height: 1.75rem;
  letter-spacing: .25px;
  font-weight: 400;
}

.blog-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 5rem;
  margin-bottom: 5rem;
}

a {
  text-decoration: none;
}
</style>