<template>
<v-app>
    <div class="page">
    <Header />
    <nuxt></nuxt>
    <Footer />
  </div>
</v-app>
</template>

<script>
export default {
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
</style>