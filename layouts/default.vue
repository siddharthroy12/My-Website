<template>
<v-app>
  <div class="page">
    <Header />
    <nuxt></nuxt>
    <Footer />
    <v-fab-transition>
      <v-btn elevation="1" fab class="up-btn" href="#header" v-if="showUpButton">
        <v-icon>mdi-chevron-up</v-icon>
      </v-btn>
    </v-fab-transition>
  </div>
</v-app>
</template>

<script>
export default {
  head: {
    script: [
      {
        src: 'https://identity.netlify.com/v1/netlify-identity-widget.js'
      }
    ]
  },
  data() {
    return {
      showUpButton: false
    }
  },
  methods: {
    handleScroll() {
      this.showUpButton = window.scrollY > 100 ? true : false
    }
  },
  created() {
    if (process.client) {
      window.addEventListener('scroll', this.handleScroll);
    }
  },
  destroyed() {
    if (process.client) {
      window.removeEventListener('scroll', this.handleScroll);
    }
  }
}
</script>

<style scoped>
* {
  font-family: "Roboto",sans-serif;
  color: white;
}

.page {
  background-color: #121212;
}

.up-btn {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
}
</style>