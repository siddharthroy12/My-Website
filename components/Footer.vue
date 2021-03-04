<template>
  <footer class="footer">
    <ul class="links">
      <li>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <a
              href="https://github.com/siddharthroy12"
              target="_blank"
              v-bind="attrs"
              v-on="on">
              <v-icon>mdi-github</v-icon>
            </a>
          </template>
          <span>siddharthroy12</span>
        </v-tooltip>
      </li>
      <li>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <a
              href="https://twitter.com/Siddharth_Roy12"
              target="_blank"
              v-bind="attrs"
              v-on="on">
              <v-icon>mdi-twitter</v-icon>
            </a>
          </template>
          <span>@Siddharth_Roy12</span>
        </v-tooltip>
      </li>
      <li>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <a
              href="mailto:siddharthroy36912@gmail.com"
              target="_blank"
              v-bind="attrs"
              v-on="on">
              <v-icon>mdi-email</v-icon>
            </a>
          </template>
          <span>siddharthroy36912@gmail.com</span>
        </v-tooltip>
      </li>
    </ul>
    <p class="hostname">
      {{ hostname }}
    </p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      hostname: !process.server ? window.location.hostname : 'Loading'
    }
  }
}
</script>

<style>

.footer {
  background-color: #101010;
  padding: 5rem;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.links {
  list-style: none;
  display: flex;
  padding: 0 !important;
}

.links li {
  margin: 0 1rem;
}

.links a {
  text-decoration: none;
}

.links i {
  font-size: 2rem !important;
}

.hostname {
  margin: 2rem 0;
}

</style>