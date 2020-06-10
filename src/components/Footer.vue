<template>
  <div class="container-fluid p-0 m-0">
    <footer class="footer">
      <div class="row justify-content-center align-items-center m-0 p-0 pt-4 pb-4 footer">
        <div class="col-lg-7 col-md-7 col-sm-12 footer-text mt-2">
          <span>&copy; 2020 design and built by Favour Vivian Woka</span>
        </div>
        <div class="col-lg-2 col-md-2 col-sm-12 social mt-2">
          <a href="https://web.facebook.com/favour.emma.3150/" target="_blank">Facebook</a>
          <a href="https://twitter.com/Fey_vik" target="_blank">Twitter</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss" scoped>
footer {
  background-color: #3a8fff;
  min-height: 10vh;
  width: 100%;
  color: #ffffff;
  font-size: 14px;
  .footer {
    min-height: 10vh;
    width: 100%;
    a {
      text-decoration: none;
      color: #ffffff;
      padding: 10px;
    }
  }
}
@media screen and (max-width: 767px) {
  footer {
    text-align: center;
  }
}
</style>