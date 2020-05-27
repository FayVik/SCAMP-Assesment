<template>
  <div class="container mt-5">
    <div class="card pb-3">
      <div class="card-body">
        <div class="overflow-auto summary">
          <b-col lg="6" class="my-1">
            <b-form-group
              label="Filter"
              label-cols-sm="3"
              label-align-sm="right"
              label-size="sm"
              label-for="filterInput"
              class="mb-0"
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

          <b-table
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
    setInterval(() => {
      this.getCountrySta();
    }, 30000);
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
    .b-table {
      color: #efefef;
      margin-top: 4%;
    }
    .pagination {
      justify-content: center;
      padding-left: 0;
    }
    hr {
      background-color: #ffffff;
      font-weight: bolder;
    }
  }
}
</style>>
