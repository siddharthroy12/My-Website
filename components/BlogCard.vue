<template>
  <nuxt-link class="_container" :to="`/blog/${slug}`">
    <v-hover v-slot='{ hover }'>
      <v-card :elevation="hover ? 12 : 2" class="blog-card">
        <img :src="banner"/>
        <div class="padding">
          <h5>{{ title }}</h5>
          <p>{{ desc }}</p>
        </div>
      </v-card>
    </v-hover>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    banner: String,
    title: String,
    desc: String,
    slug: String,
  },

  methods: {
    slugToLink(slug) {
      return `/blog/${slug}`
    },
  }
}
</script>

<style scoped>
._container {
  display: block;
  width: 40%;
  margin: 1rem;
}

.blog-card {
  transition: all ease 100ms;
}

img {
  width: 100%
}

.padding {
  padding: 1rem;
}

h5 {
  font-size: 1.3rem;
}

p {
  margin-bottom: 0 !important;
  margin-top: 1rem;
}

@media (max-width: 630px) {
  ._container {
    width: 100%;
  }
}
</style>