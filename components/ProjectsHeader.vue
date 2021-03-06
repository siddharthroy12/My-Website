<template>
  <div class="_container">
	  <v-card class="card" elevation="2">
      <div class="header-icon-wrapper">
        <div class="header-icon">
          <v-icon>mdi-code-tags</v-icon>
        </div>
      </div>
      <div class="text">
        <p>From Web Apps and Mobile Apps to Games, check out my latest web projects.</p>
      </div>
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
  margin-top: 150px;
}

.card {
  width: 100%;
	max-width: 50rem !important;
  background-color: #1E1E1E !important;
  color:white !important;
  text-align: center;
}

.header-icon {
  width: 200px;
  height: 200px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #1E1E1E;
}

.header-icon i {
  font-size: 5rem !important;
}

.header-icon-wrapper {
  display: flex;
  justify-content: center;
  position: relative;
  top: -100px
}

.text {
  position: relative;
  top: -50px;
  font-size: 1.3rem;
}

</style>