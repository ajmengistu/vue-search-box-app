<template>
  <div class="home">
    <SearchBox v-on:search-query="fetchSearchQuery" />
  </div>
</template>

<script>
// @ is an alias to /src
import SearchBox from "@/components/commons/SearchBox";

export default {
  name: "Home",
  components: {
    SearchBox,
  },
  data() {
    return {
      queryResults: [],
      wikiQueryResults: [],
    };
  },
  methods: {
    fetchSearchQuery(query) {
      console.log(query);
      this.searchWiki(query);
    },
    searchWiki(query) {
      console.log(query)
    }
  },
};
</script>

<style scoped>
</style>