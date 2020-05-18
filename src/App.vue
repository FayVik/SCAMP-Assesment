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
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300&family=Roboto:wght@500&display=swap");
#app {
  font-family: "Oswald", sans-serif;
  margin: 0;
  padding: 0;
  background: url("./assets/map.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: 30%;
  min-height: 99.5vh;
  background-attachment: fixed;
}
</style>
