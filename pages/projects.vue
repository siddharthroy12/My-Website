<template>
  <div>
    <ProjectsHeader :desc="description"/>
    <AllProjects />
  </div>
</template>

<script>
export default {
  head() {
    return {
      titleTemplate: '%s - Projects',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.description
        }
      ]
    }
  },

  data() {
    return {
      description: 'From Web Apps and Mobile Apps to Games, check out my latest projects.'
    }
  }
}
</script>

<style scoped>

</style>