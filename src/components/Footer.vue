<template>
  <div class="container-fluid p-0 m-0">
    <footer class="footer">
      <div class="row justify-content-center align-items-center m-0 p-0 footer">
        <div class="col-7">
          <span>@copy write 2020</span>
        </div>
        <div class="col-2">
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
</style>