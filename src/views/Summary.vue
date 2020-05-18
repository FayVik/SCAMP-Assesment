<template>
  <div class="container mt-5">
    <div class="card pb-3">
      <div class="card-body">
        <div class="overflow-auto summary">
          <b-table
            id="my-table"
            :items="items"
            :per-page="perPage"
            :current-page="currentPage"
            small
          ></b-table>

          <hr />
          <b-pagination
            v-model="currentPage"
            :total-rows="rows"
            :per-page="perPage"
            aria-controls="my-table"
          ></b-pagination>
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
      currentPage: 1,
      perPage: 6,
      items: []
    };
  },
  mounted() {
    this.getCountrySta();
  },
  methods: {
    async getCountrySta() {
      try {
        const response = await fetch("https://api.covid19api.com/summary");
        const data = await response.json();
        setInterval(() => {
          this.items = data.Countries;
        }, 1000);
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
.card {
  background: rgb(58, 143, 255);
  color: #ffffff;
  .summary {
    min-height: 40vh;
    .b-table {
      color: #183577;
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
