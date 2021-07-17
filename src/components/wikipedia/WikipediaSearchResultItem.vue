<template>
  <div class="container">
    <a
      v-bind:href="'https://wikipedia.com/wiki/' + result.title"
      target="_blank"
    >
      <h5>{{ result.title }}</h5>
    </a>
    <p v-html="result.snippet">{{ result.snippet }}</p>
  </div>
</template>


<script>
export default {
  name: "WikipediaSearchResultItem",
  props: ["result"],
  method: {},
};
</script>


<style scoped>
</style>