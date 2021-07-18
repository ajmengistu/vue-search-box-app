<template>
  <div class="container mt-4">
    <h3>TMDB</h3>
    <div v-bind:key="result.id" v-for="result in tmdbSearchResults">
      <TMDBSearchResultItem v-bind:result="result" />
    </div>
  </div>
</template>

<script>
import TMDBSearchResultItem from "@/components/tmdb/TMDBSearchResultItem";

export default {
  name: "TMDBSearchResultList",
  components: {
    TMDBSearchResultItem,
  },
  props: ["tmdbSearchResults"],
};
</script>


<style scoped>
</style>