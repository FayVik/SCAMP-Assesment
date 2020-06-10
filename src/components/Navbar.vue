<template>
  <div class="col-lg-12 col-md-12 col-sm-12 text-center navbar-logo p-0 m-0 fixed-top shadow">
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
  font-size: 18px;
  color: rgb(255, 255, 255);
  background-color: #3a8fff;
  width: 100%;
  img {
    width: 50px;
  }
}
</style>