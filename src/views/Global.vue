<template>
  <div class="container text-center">
    <div class="card" style="width: 100%;">
      <div class="card-body">
        <div class="row align-items-center global" v-if="Global">
          <div class="col-lg-4 mt-2 text-center">
            <h2>{{Global.TotalConfirmed}}</h2>
            <p class="card-text">Confirmed</p>
          </div>
          <div class="col-lg-4 mt-2 text-center">
            <h1>{{Global.TotalRecovered}}</h1>
            <p class="card-text">Recovered</p>
          </div>
          <div class="col-lg-4 mt-2 text-center">
            <h2>{{Global.TotalDeaths}}</h2>
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
    }
    // formatNumber() {
    //   const death = data.Global.TotalDeaths;
    //   return death.toString().replace(/(\d)(?=(\d{3})+(?!\d))/g, "$1,");
    // }
  }
};
</script>
<style lang="scss" scoped>
h2 {
  color: rgb(58, 143, 255);
  font-size: 30px;
  font-weight: bolder;
}
h1 {
  font-size: 80px;
  color: rgb(58, 143, 255);
  font-weight: bolder;
}
p {
  color: #183577;
}
.global {
  min-height: 40vh;
}
</style>
