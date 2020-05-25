<template>
  <div id="app">
    <Home />
  </div>
</template>
<script>
import Home from "./views/Home.vue";
export default {
  name: "app",
  components: {
    Home
  }
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap");
#app {
  font-family: "Montserrat", sans-serif;
  margin: 0;
  padding: 0;
  background: linear-gradient(
      rgba(238, 238, 238, 0.875),
      rgba(238, 238, 238, 0.875)
    ),
    url("./assets/map.png");
  background-position: cover;
  background-repeat: no-repeat;
  background-size: 100%;
  min-height: 99.5vh;
  background-attachment: fixed;
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
}
</style>
