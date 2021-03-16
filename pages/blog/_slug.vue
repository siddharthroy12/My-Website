<template>
  <article>
    <h1>{{blog.title}}</h1>
    <div class="banner-container">
      <img class="banner" :src="require(`~/${assetPath(blog.banner)}`)" alt="Banner">
      <a class="banner-source" :href="blog.banner_source" rel="noreferrer">Source of the picture</a>
    </div>
    <nuxt-content :document="blog"/>
  </article>
</template>

<script>
export default {
  head() {
    return {
      title: this.blog.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.stripContent(this.blog)
        }
      ]
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
    
    assetPath(src) {
      return src.slice(1, src.length)
    },
  },

  async asyncData({ params, $content }) {
    const blogs = await $content('blogs').where({slug: params.slug}).fetch()
    console.log(blogs[0])
    return { blog: blogs[0] }
  },
}
</script>

<style scoped>
article {
  max-width: 50rem;
  margin-left: auto;
  margin-right: auto;
  padding: 0 1.5rem;
  margin-bottom: 5rem;
}

h1 {
  text-align: center;
  font-size: 2rem;
  margin: 3rem 0;
}

.banner-container {
  margin-bottom: 4rem;
}

.banner {
  display: block;
  width: 80%;
  margin-left: auto;
  margin-right: auto;
}

.banner-source {
  color: #c9c9c9;
  text-align: center;
  display: block;
}
</style>