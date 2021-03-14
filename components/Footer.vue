<template>
  <footer class="footer" id="contact">
    <ul class="links">
      <li>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <a
              href="https://github.com/siddharthroy12"
              target="_blank"
              rel="noreferrer"
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
              rel="noreferrer"
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
              rel="noreferrer"
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
      © {{ hostname }}
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
  background-color: #212121;
  padding: 2rem;
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
  color: #fff;
  opacity: 0.8;
}

.links i {
  font-size: 2rem !important;
}

.hostname {
  margin-bottom: 0 !important;
  margin-top: 1rem;
}

</style>