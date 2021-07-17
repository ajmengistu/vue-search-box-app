<template>
  <div class="container mt-4">
    <h3>Wikipedia</h3>
    <div v-bind:key="result.pageid" v-for="result in wikipediaSearchResults">
      <WikipediaSearchResultItem v-bind:result="result" />
    </div>
  </div>
</template>

<script>
import WikipediaSearchResultItem from "@/components/wikipedia/WikipediaSearchResultItem";

export default {
  name: "WikipediaSearchResultList",
  components: {
    WikipediaSearchResultItem,
  },
  props: ["wikipediaSearchResults"],
};
</script>


<style scoped>
</style>