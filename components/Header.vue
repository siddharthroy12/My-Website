<template>
  <header>
      <nav>
        <ul>
          <li>
            <NuxtLink to="/">
              <v-btn depressed class="nav-btn" >
                Home
              </v-btn>
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/projects">
              <v-btn depressed class="nav-btn" >
                Projects
              </v-btn>
            </NuxtLink>
          </li>
          <li>
            <v-btn depressed class="nav-btn">
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
  font-size: 1rem;
}
</style>