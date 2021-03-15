<template>
  <article>
    <h1>{{blog.title}}</h1>
    <div class="banner-container">
      <img class="banner" :src="require(`~/${assetPath(blog.banner)}`)">
    </div>
    <nuxt-content :document="blog"/>
  </article>
</template>

<script>
export default {
  methods: {
    assetPath(src) {
      return src.slice(1, src.length)
    },
  },
  async asyncData({ params, $content }) {
    const blogs = await $content('blogs').where({slug: params.slug}).fetch()
    console.log(blogs[0])
    return { blog: blogs[0] }
  }
}
</script>

<style scoped>
article {
  max-width: 50rem;
  margin-left: auto;
  margin-right: auto;
}

h1 {
  text-align: center;
  font-size: 2rem;
  margin: 3rem 0;
}

.banner-container {
  padding: 0 5rem;
}

.banner {
  display: block;
  width: 100%;
}
</style>