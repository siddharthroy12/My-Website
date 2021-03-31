<template>
  <header id="header">
      <nav>
        <ul>
          <li>
            <v-btn depressed class="nav-btn" nuxt="true" to="/">
              Home
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn" nuxt="true" to='/projects'>
              Projects
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn" nuxt="true" to='/blog'>
              Blog
            </v-btn>
          </li>
          <li>
            <v-btn depressed class="nav-btn" href="#contact">
              Contact
            </v-btn>
          </li>
        </ul>
      </nav>
    </header>
</template>

<script>
export default {

}
</script>

<style scoped>
header {
  margin-top: 2rem;
  background-color: #121212;
  padding: 1rem;
  display: flex;
  justify-content: center;
}

ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 0 !important;
}

li {
  list-style: none;
  margin: 0.5rem;
}

li a {
  text-decoration: none;
}

.nav-btn {
  background-color: #121212 !important;
  color: white;
  font-size: 1.2rem;
}
</style>