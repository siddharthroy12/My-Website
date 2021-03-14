<template>
<div role="group" class="_container">
  <v-card elevation="2" class="card">
    <v-card-title>
      <v-icon class="title-icon">mdi-code-tags</v-icon>Featured Projects
    </v-card-title>
    <v-divider class="theme--dark"/>
    <v-card-text style="width: 100%">
      <div class="content">
        <ProjectCard
			    v-for="(project, index) in projects" :key="index"
          :project="project"
		    />
      </div>
    </v-card-text>
  </v-card>
</div>
  
</template>

<script>
export default {
  data() {
    return {
      projects: []
    }
  },

  async fetch() {
		const projects = await this.$content('projects').where({featured: true}).fetch()
		this.projects = projects
	}
}
</script>

<style scoped>
._container {
  display: flex;
  justify-content: center;
  margin-top: 50px;
  margin-bottom: 50px;
}

.card {
  width: 100%;
  max-width: 50rem !important;
  background-color: #1E1E1E !important;
  color:white !important;
}

.title-icon {
  color: white !important;
  margin-right: 1rem;
}

.content {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>