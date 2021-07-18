<template>
  <div class="mt-4">
    <a v-bind:href="'https://youtube.com/watch?v=' + result.id" target="_blank">
      <img v-bind:src="result.snippet.thumbnails.default.url" />
    </a>
    <!-- <div v-html="result.snippet"></div> -->
    <span>| {{ result.snippet.title }} | {{ result.snippet.description.substring(0,120)}}</span>
  </div>
</template>


<script>
export default {
  name: "YouTubeSearchResultItem",
  props: ["result"],
  method: {},
};
</script>

<style scoped>
</style>