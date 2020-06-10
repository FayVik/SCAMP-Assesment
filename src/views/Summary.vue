<template>
  <div class="container mt-5">
    <div class="card pb-3">
      <div class="card-body">
        <div class="col-12 summary">
          <b-col class="m-auto col-lg-6 col-md-12 col-sm-12">
            <b-form-group
              label="Filter"
              label-cols-sm="2"
              label-align-sm="left"
              label-size="sm"
              label-for="filterInput"
              class="m-0"
            >
              <b-input-group size="sm">
                <b-form-input
                  v-model="filter"
                  type="search"
                  id="filterInput"
                  placeholder="Type to Search"
                ></b-form-input>
                <b-input-group-append>
                  <b-button :disabled="!filter" @click="filter = ''">Clear</b-button>
                </b-input-group-append>
              </b-input-group>
            </b-form-group>
          </b-col>
          <hr />
          <b-table
            class="mt-3 table-responsive"
            :filter="filter"
            :items="items"
            :per-page="perPage"
            :fields="fields"
            :current-page="currentPage"
            small
          ></b-table>

          <hr />
          <b-pagination v-model="currentPage" :total-rows="rows" :per-page="perPage"></b-pagination>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "summary",
  data() {
    return {
      filter: null,
      currentPage: 1,
      perPage: 6,
      fields: [
        "Country",
        "NewConfirmed",
        "TotalConfirmed",
        "NewDeaths",
        "TotalDeaths",
        "NewRecovered",
        "TotalRecovered"
      ],
      items: []
    };
  },
  mounted() {
    this.getCountrySta();
    // setInterval(() => {
    //   this.getCountrySta();
    // }, 30000);
  },
  methods: {
    async getCountrySta() {
      try {
        const response = await fetch("https://api.covid19api.com/summary");
        const data = await response.json();
        this.items = data.Countries;
      } catch (error) {
        console.error(error);
      }
    }
  },
  computed: {
    rows() {
      return this.items.length;
    }
  }
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");
.card {
  background: rgb(58, 143, 255);
  color: #ffffff;
  font-size: 18px;
  .summary {
    min-height: 40vh;
    .table-responsive {
      color: #fff !important;
    }
    .pagination {
      justify-content: center;
    }
    hr {
      background-color: #ffffff;
      font-weight: bolder;
    }
  }
}
</style>
