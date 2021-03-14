<template>
<div role="main" class="_container">
  <v-card elevation="2" class="card">
    <div class="content">
      <div class="profile-wrapper">
        <img
          src="/img/profilepic.jpg"
          class="profile"
          alt="profile-pic"
        >
        <div class="name">
          Siddharth Roy
        </div>
      </div>
      <div class="body-wrapper">
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
	max-width: 50rem !important;
  background-color: #1E1E1E !important;
  color:white !important;
}

.profile-wrapper {
  position: relative;
  top: -100px;
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.body-wrapper {
  position: relative;
  top: -100px;
}

.profile {
  width: 200px;
  height: 200px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
  border-radius: 50%;
}

.name {
  text-align: center;
  margin: 3rem 0;
  font-size: 1.8rem;
}

.chips {
  display: block;
  text-align: center;
}

.chips span {
  margin: 1rem 0.6rem;
}

.desc {
  text-align: center;
  margin: 3rem 4rem;
  color: #c9c9c9;
  word-spacing: 5px;
  font-size: 1.2rem;
}

p {
  margin: 1rem 0 0;
}

.tech-chips {
  display: block;
  text-align: center;
  justify-content: center;
}

.tech-chip {
  border-color: hsla(0,0%,100%,.12) !important;
  color: white !important;
  margin: 1rem 0.3rem;
}

</style>