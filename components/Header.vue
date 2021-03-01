<template>
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