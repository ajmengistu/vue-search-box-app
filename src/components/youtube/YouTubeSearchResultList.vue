<template>
  <div class="container mt-4">
    <h3>YouTube</h3>
    <div v-bind:key="result.etag" v-for="result in youtubeSearchResults">
      <YouTubeSearchResultItem v-bind:result="result" />
    </div>
  </div>
</template>

<script>
import YouTubeSearchResultItem from "@/components/youtube/YouTubeSearchResultItem";

export default {
  name: "YouTubeSearchResultList",
  components: {
    YouTubeSearchResultItem,
  },
  props: ["youtubeSearchResults"],
};
</script>


<style scoped>
</style>