<template>
  <div class="home">
    <div class="container mt-4">
      <div class="row">
        <div class="col">
          <YouTubeSearchResultList v-bind:youtubeSearchResults="youtubeQueryResults" />
        </div>
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
import YouTubeSearchResultList from '@/components/youtube/YouTubeSearchResultList';
import axios from "axios";

export default {
  name: "Home",
  components: {
    SearchBox,
    WikipediaSearchResultList,
    TMDBSearchResultList,
YouTubeSearchResultList
  },
  data() {
    return {
      queryResults: [],
      // wikiQueryResults: [],
      tmdbQueryResults: [],
      youtubeQueryResults: []
    };
  },
  methods: {
    fetchSearchQuery(query) {
      this.searchWiki(query);
      this.searchTMDB(query);
      this.searchYouTube(query);
    },
    searchYouTube(query) {
      axios
        .get(
                   // `https://www.googleapis.com/youtube/v3/search?part=snippet&maxResults=5&q=${query}&key=AIzaSyDEo3Pw-0ZZ_F4sPWadom9CE1ISNQKivy0`
 `https://en.wikipedia.org/w/api.php?action=query&format=json&origin=*&list=search&srsearch=${query}`
        )
        .then((res) => {
          this.youtubeQueryResults = res.data.query.search;
          this.youtubeQueryResults = this.queryResults.slice(0, 5); // grab on first top 5 search results
        })
        .catch((err) => console.log(err));

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
          console.log(res.data.results);
          this.tmdbQueryResults = this.tmdbQueryResults.slice(0, 5);
        })
        .catch((err) => console.log(err));
    },
  },
  // show the latest movie releases and trending YouTube Videos at initial load.
  created() {
    axios
      .get(
        `https://api.themoviedb.org/3/trending/all/day?api_key=1a7eb2f78daf0c6f300f6b339f4f5030`
      )
      .then((res) => {
        this.tmdbQueryResults = res.data.results;
        console.log(res.data.results);
        this.tmdbQueryResults = this.tmdbQueryResults.slice(0, 5);
      })
      .catch((err) => console.log(err));


      axios
        .get(
        `https://www.googleapis.com/youtube/v3/videos?chart=mostPopular&key=AIzaSyDEo3Pw-0ZZ_F4sPWadom9CE1ISNQKivy0&part=snippet&maxResults=5`)
        .then((res) => {
          console.log(res)
          this.youtubeQueryResults = res.data.items;
          // this.youtubeQueryResults = this.queryResults.slice(0, 5); // grab on first top 5 search results
        })
        .catch((err) => console.log(err));
  },
};
</script>

<style scoped>
</style>