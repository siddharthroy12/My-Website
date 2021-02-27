<template>
<div role="hero" class="_container">
  <v-card elevation="2" class="card">
    <div class="content">
      <div class="profile-wrapper">
        <img
          src="https://siddharthroy.pythonanywhere.com/static/base/img/profilepic.jpg"
          class="profile">
        <div class="name">
          Siddharth Roy
        </div>
      </div>
      <div class="chips">
        <v-chip>
          Frontend Developer
        </v-chip>
        <v-chip>
          Backend Developer
        </v-chip>
        <v-chip>
          Mobile Developer
        </v-chip>
      </div>
      <div class="desc">
        <p>
          I design simple beautiful software Applications ranging from <b>Websites</b>,
          <b>Blogs</b> to <b>Android Apps</b> using a variety software Technologies
          such as <b>Nuxt/Vuejs</b> , <b>React</b>, <b>React Native</b>, <b>Django</b>.
        </p>
        <p>
          I am a fast learner and also have the ability to tackle problems by myself.
        </p>
      </div>
      <div class="tech-chips">
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-vuejs</v-icon>Vue
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-nuxt</v-icon>Nuxt
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-nodejs</v-icon>Nodejs
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-react</v-icon>React
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-react</v-icon>React Native
        </v-chip>
        <v-chip outlined class="tech-chip">
          Django
        </v-chip>
      </div>
      <div class="tech-chips">
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-language-javascript</v-icon>Javascript
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-language-typescript</v-icon>Typescript
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-language-python</v-icon>Python
        </v-chip>
        <v-chip outlined class="tech-chip">
          <v-icon>mdi-language-cpp</v-icon>
        </v-chip>
      </div>
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
  height: 40rem;
	max-width: 50rem !important;
  padding: 1rem;
  background-color: #1E1E1E;
  color:white;
}

.content {
  position: relative;
  top: -120px;
}

.profile-wrapper {
  
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.profile {
  width: 200px;
  height: 200px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  border-radius: 50%;
}

.name {
  text-align: center;
  margin: 2rem 0;
  font-size: 1.8rem;
}

.chips {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 1rem 0;
}

.desc {
  text-align: center;
  margin: 3rem 5rem;
  color: #c9c9c9;
  word-spacing: 5px;
  font-size: 1.2rem;
}

p {
  margin: 1rem 0;
}

.tech-chips {
  display: flex;
  justify-content: center;
  margin: 0rem 6rem;
  gap: 10px;
}

.tech-chip {
  border-color: hsla(0,0%,100%,.12);
  color: white;
  margin: 1rem 0;
}

</style>