<template>
  <div class="home">
    <div class="container mt-4">
      <div class="row">
        <div class="col">1 of 3</div>
        <div class="col">
          <SearchBox v-on:search-query="fetchSearchQuery" />
          <WikipediaSearchResultList
            v-bind:wikipediaSearchResults="queryResults"
          />
        </div>
        <div class="col">
          <TMDBSearchResultList v-bind:tmdbSearchResults="tmdbQueryResults" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SearchBox from "@/components/commons/SearchBox";
import WikipediaSearchResultList from "@/components/wikipedia/WikipediaSearchResultList";
import TMDBSearchResultList from "@/components/tmdb/TMDBSearchResultList";
import axios from "axios";

export default {
  name: "Home",
  components: {
    SearchBox,
    WikipediaSearchResultList,
    TMDBSearchResultList,
  },
  data() {
    return {
      queryResults: [],
      // wikiQueryResults: [],
      tmdbQueryResults: [],
    };
  },
  methods: {
    fetchSearchQuery(query) {
      this.searchWiki(query);
      this.searchTMDB(query);
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
    searchTMDB(query) {
      axios
        .get(
          `https://api.themoviedb.org/3/search/multi?api_key=1a7eb2f78daf0c6f300f6b339f4f5030&language=en-US&query=${query}&page=1&include_adult=false`
        )
        .then((res) => {
          this.tmdbQueryResults = res.data.results;
          console.log(res.data.results)
          this.tmdbQueryResults = this.tmdbQueryResults.slice(0, 5);
        })
        .catch((err) => console.log(err));
    },
  },
  // show the latest movie releases and trending YouTube Videos at initial load.
    created() {
      axios
        .get(
          `https://en.wikipedia.org/w/api.php?action=query&format=json&origin=*&list=search&srsearch=China`
        )
        .then((res) => {
          this.queryResults = res.data.query.search;
          this.queryResults = this.queryResults.slice(0, 5); // grab on first top 5 search results
        })
        .catch((err) => console.log(err));
    }
};
</script>

<style scoped>
</style>