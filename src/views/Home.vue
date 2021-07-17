<template>
  <div class="home">
    <div class="container mt-4">
      <div class="row">
        <div class="col">1 of 3</div>
        <div class="col-6">
          <SearchBox v-on:search-query="fetchSearchQuery" />
          <WikipediaSearchResultList
            v-bind:wikipediaSearchResults="queryResults"
          />
        </div>
        <div class="col">3 of 3</div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SearchBox from "@/components/commons/SearchBox";
import WikipediaSearchResultList from "@/components/wikipedia/WikipediaSearchResultList";
import axios from "axios";

export default {
  name: "Home",
  components: {
    SearchBox,
    WikipediaSearchResultList,
  },
  data() {
    return {
      queryResults: [],
      // wikiQueryResults: [],
    };
  },
  methods: {
    fetchSearchQuery(query) {
      this.searchWiki(query);
    },
    searchWiki(query) {
      axios
        .get(
          `https://en.wikipedia.org/w/api.php?action=query&format=json&origin=*&list=search&srsearch=${query}`
        )
        .then((res) => {
          this.queryResults = res.data.query.search;
          this.queryResults = this.queryResults.slice(0, 5); // grab on first top 5 search results
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style scoped>
</style>