<template>
<v-hover v-slot='{ hover }'>
  <v-card :elevation="hover ? 12 : 2" class="project-card">
    <v-card-title>{{ project.title }}</v-card-title>
    <v-card-text class="desc">
      {{ project.desc }}
    </v-card-text>
    <v-card-subtitle class="techs">
      <v-chip v-for="tech in techStack" :key="tech" class="tech-chip" outlined>
        <v-icon v-if="tech === 'Vue'">mdi-vuejs</v-icon>
        <v-icon v-if="tech === 'Nuxt'">mdi-nuxt</v-icon>
        <v-icon v-if="tech === 'Nodejs'">mdi-nodejs</v-icon>
        <v-icon v-if="tech === 'Javascript'">mdi-language-javascript</v-icon>
        <v-icon v-if="tech === 'React' || tech === 'React Native'">mdi-react</v-icon>
        <v-icon v-if="tech === 'Cpp'">mdi-language-cpp</v-icon>
        <v-icon v-if="tech === 'Typescript'">mdi-language-typescript</v-icon>
        <v-icon v-if="tech === 'Python'">mdi-language-python</v-icon>
        <v-icon v-if="tech === 'Bootstrap'">mdi-bootstrap</v-icon>
        <span v-if="tech !== 'Cpp'">
          {{ tech }}
        </span>
      </v-chip>
    </v-card-subtitle>
    <v-divider class="theme--dark"/>
    <v-card-actions>
      <v-btn class="project-btn" depressed :href="project.code" target="_blank">
        <v-icon>mdi-code-tags</v-icon>
        <p>Code</p>
      </v-btn>
      <v-btn class="project-btn" depressed :href="project.live" target="_blank">
        <v-icon>mdi-eye</v-icon>
        <p>Live</p>
      </v-btn>
    </v-card-actions>
  </v-card>
</v-hover>
</template>

<script>
export default {
  props: {
    project: Object
  },

  data() {
    return {
      techStack: []
    }
  },

  async fetch() {
    this.techStack = this.project.stack.split(',')
  }
}
</script>

<style scoped>
.project-card {
  background-color: #1E1E1E !important;
  color:white !important;
  width: 45%;
  margin: 0.9rem;
  transition: all ease 100ms;
  height: fit-content;
}

.desc {
  color: #c9c9c9 !important;
}

.tech-chip {
  font-size: 0.8rem;
  border-color: hsla(0,0%,100%,.12) !important;
  color: white !important;
  background-color: #1E1E1E !important;
  margin-right: 0.4rem;
  margin-bottom: 0.4rem;
}

.project-btn {
  background-color: #1e1e1e !important;
  color: white;
  font-size: 0.8rem;
  display: flex;
}

.project-btn p {
  margin: 0 5px;
}

@media (max-width: 760px) {
  .project-card {
    width: 100% !important;
  }
}
</style>