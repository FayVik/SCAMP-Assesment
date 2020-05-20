<template>
  <div class="container text-center">
    <div class="card" style="width: 100%;">
      <div class="card-body">
        <div class="row align-items-center global" v-if="Global">
          <div class="col-lg-4 mt-2 text-center">
            <h2>{{formatNumberWithCommas(Global.TotalConfirmed)}}</h2>
            <p class="card-text">Confirmed</p>
          </div>
          <div class="col-lg-4 mt-2 text-center">
            <h1>{{formatNumberWithCommas(Global.TotalRecovered)}}</h1>
            <p class="card-text">Recovered</p>
          </div>
          <div class="col-lg-4 mt-2 text-center">
            <h2>{{formatNumberWithCommas(Global.TotalDeaths)}}</h2>
            <p class="card-text">Deaths</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Global",
  data() {
    return {
      Global: {}
    };
  },
  mounted() {
    this.getEmployees();
  },
  methods: {
    async getEmployees() {
      try {
        const response = await fetch("https://api.covid19api.com/summary");
        const data = await response.json();
        setInterval(() => {
          this.Global = data.Global;
        }, 1000);
      } catch (error) {
        console.error(error);
      }
    },
    formatNumberWithCommas(x) {
      return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }
  }
};
</script>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");
h2 {
  color: rgb(58, 143, 255);
  font-size: 30px;
  font-family: "Bebas Neue", cursive;
}
.card-text {
  font-family: "Bebas Neue", cursive;
}
h1 {
  font-size: 80px;
  color: rgb(58, 143, 255);
  font-family: "Bebas Neue", cursive;
}
p {
  color: #183577;
}
.global {
  min-height: 40vh;
}
</style>
