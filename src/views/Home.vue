<template>
  <div class="container-fluid p-0 m-0">
    <div class="row p-0 m-0 justify-content-around align-items-center">
      <div class="col-12 text-center navbar-logo">
        <div class="fixed text-center pt-1">
          Covid-19
          <img src="../assets/covid-logo.png" alt />
          Update
        </div>
      </div>
      <div class="col-12 hero-page">
        <div class="container text-center hero-page-content">
          <div class="row hero-page-content-details">
            <div class="col-lg-4 col-sm-12 col-md-4">
              <p>Total Case</p>
            </div>
            <div class="col-lg-4 col-sm-12 col-md-4">
              <p>Recovered Case</p>
            </div>
            <div class="col-lg-4 col-sm-12 col-md-4">
              <p>Death Case</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  // data() {
  //   total: [];
  // },
  // methods: {},
  components: {}
};
</script>
<style lang="scss" scoped>
.navbar-logo {
  background: rgb(255, 255, 255);
  height: 9vh;
  text-align: center;
  font-size: 20px;
  box-shadow: 0 4px 0 rgb(138, 138, 138);
  img {
    width: 4%;
    text-align: center;
  }
}
.hero-page {
  background: linear-gradient(rgb(203, 59, 57), rgb(203, 59, 57));
  // background-position: 50% 50%;
  // background-repeat: no-repeat;
  // background-size: 345px 412px;
  width: 100%;
  height: 91.1vh;
  // background-attachment: fixed;
  // color: #fff;
  .hero-page-content {
    background: url("../assets/map.png");
    background-position: 50% 50%;
    background-repeat: no-repeat;
    background-size: 345px 412px;
    width: 100%;
    height: 91.1vh;
    background-attachment: fixed;
    color: #fff;
    .hero-page-content-details {
      height: 91.1vh;
      justify-content: space-around;
      align-items: center;
    }
  }
}
</style>