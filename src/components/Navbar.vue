<template>
  <div class="col-12 text-center navbar-logo p-0 m-0 fixed-top shadow">
    <div class="text-center pt-3">
      COVID-19
      <img src="../assets/covid-logo.png" alt />
      UPDATE
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar"
};
</script>

<style lang="scss" scoped>
.navbar-logo {
  height: 12vh;
  text-align: center;
  font-size: 20px;
  color: rgb(255, 255, 255);
  background-color: #3a8fff;
  img {
    width: 4%;
    text-align: center;
  }
}
</style>