<template>
  <footer class="footer">
    <v-chip large class="links">
      Hello
    </v-chip>
    {{ hostname }}
  </footer>
</template>

<script>
export default {
  data() {
    return {
      hostname: window.location.hostname
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
  width: fit-content;
}

</style>