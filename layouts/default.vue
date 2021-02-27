<template>
  <div class="page">
    <header>
      <nav>
        <ul>
          <li>
            <v-btn depressed class="nav-btn">
              Home
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn">
              Projects
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn">
              Blog
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn">
              Contact
            </v-btn>
          </li>
        </ul>
      </nav>
    </header>
    <nuxt></nuxt>
  </div>
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

header {
  background-color: #121212;
  padding: 1rem;
  display: flex;
  justify-content: center;
}

ul {
  display: flex;
  gap: 1rem;
}

li {
  list-style: none;
}

.nav-btn {
  background-color: #121212 !important;
  color: white;
  font-size: 1rem;
}

</style>