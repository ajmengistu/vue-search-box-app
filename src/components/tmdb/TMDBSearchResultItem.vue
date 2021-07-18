<template>
  <div class="container mb-4">
    <a
      v-bind:href="
        'https://www.themoviedb.org/' + result.media_type + '/' + result.id
      "
      target="_blank"
      rel="noopener noreferrer"
    >
      <img
        v-bind:src="'https://image.tmdb.org/t/p/h100' + result.poster_path"
      />
    </a>
    <span
      >| {{ result.title }} | {{ result.release_date }} |
      {{ result.vote_average }} ({{ result.vote_count }}) | {{ result.overview}} </span
    >
    <!-- <p>{{ result.overview}}</p> -->
  </div>
</template>


<script>
export default {
  name: "TMDBSearchResultItem",
  props: ["result"],
  method: {},
};
</script>

<style scoped>
</style>