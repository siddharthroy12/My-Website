<template>
<div role="projects" class="_container">
  <v-card elevation="2" class="card">
    <v-card-title>
      <v-icon class="title-icon">mdi-code-tags</v-icon>Featured Projects
    </v-card-title>
    <v-divider class="theme--dark"/>
    <v-card-text style="width: 100%">
      <div class="content">
        <ProjectCard />
        <ProjectCard />
        <ProjectCard />
      </div>
    </v-card-text>
  </v-card>
</div>
  
</template>

<script>
export default {

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

.project-card {
  background-color: #1E1E1E !important;
  color:white !important;
  width: 46%;
  margin: 1rem;
}

@media (max-width: 760px) {
  .project-card {
    width: 100% !important;
  }
}

</style>