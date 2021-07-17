<template>
  <div class="container mt-4">
    <div class="row">
      <div class="col">1 of 3</div>
      <div class="col-6">
        <form class="d-flex" @submit="searchQuery">
          <input
            v-model='query'
            class="form-control me-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
        </form>
      </div>
      <div class="col">3 of 3</div>
    </div>
  </div>
</template>


<script>
export default {
  name: "SearchBox",
    data() {
      return {
          query: ''
      };
    },
  methods: {
    searchQuery(e) {
        e.preventDefault();
        this.$emit("search-query", this.query);
    },
  },
};
</script>

