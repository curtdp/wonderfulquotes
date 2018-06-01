<template>
  <div class="bg-grey-light shadow-inner rounded overflow-hidden mb-8">
    <div :style="{width: quotesCount / maxQuotes * 100 + '%'}" class="progressBar bg-blue text-white text-center">{{ quotesCount }} / {{ maxQuotes }}</div>
  </div>
</template>

<script>
export default {
  props: ["maxQuotes", "quotesCount"]
};
</script>

<style scoped>
.progressBar {
  transition: width 0.5s ease-in-out;
  min-width: 10%;
}
</style>