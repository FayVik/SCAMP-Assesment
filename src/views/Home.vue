<template>
  <div class="container-fluid hero-page p-0 m-0">
    <Navbar />
    <div class="hero-page-content">
      <div>
        <h2 class="text-center pt-5 m-0 mb-4 mt-5">The Global Update</h2>
        <Global></Global>
      </div>
      <div>
        <h2 class="text-center pt-3 m-0 mb-4 mt-2">Per Country Update</h2>
        <Summary class="mb-5"></Summary>
      </div>
      <div class="mt-5">
        <CovidIfo />
      </div>
      <div class="mt-2">
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
import Global from "./Global";
import Summary from "./Summary";
import CovidIfo from "../components/CovidInfo";
import Navbar from "../components/Navbar";
import Footer from "../components/Footer";
export default {
  name: "Home",
  components: {
    Global,
    Summary,
    CovidIfo,
    Navbar,
    Footer
  }
};
</script>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");
.hero-page {
  width: 100%;
  min-height: 79vh;
  .hero-page-content {
    width: 100%;
    min-height: 99.8vh;
  }
}
h2 {
  color: #183577;
  font-weight: normal;
  text-transform: uppercase;
  font-family: "Bebas Neue", cursive;
}
</style>
