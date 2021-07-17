<template>
  <div>
    <form class="d-flex" @submit="searchQuery">
      <input
        v-model="query"
        class="form-control me-2"
        type="search"
        placeholder="Search"
        aria-label="Search"
      />
    </form>
  </div>
</template>


<script>
export default {
  name: "SearchBox",
  data() {
    return {
      query: "",
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

