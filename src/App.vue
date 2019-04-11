<template>
  <div id="app">
    <img class="logo" alt="Vue logo" src="./assets/logo.png">
    <Gravatar/>
  </div>
</template>

<script>
import Gravatar from "./components/Gravatar.vue";

export default {
  name: "app",
  components: {
    Gravatar
  }
};
</script>

<style scoped>
.logo {
  width: 200px;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
