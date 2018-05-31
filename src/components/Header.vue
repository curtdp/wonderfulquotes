<template>
  <div>
    <h1>Цитат добавлено</h1>
    <div class="progress-wrapper">
      <div class="progress flex w-full h-6 bg-grey shadow-inner rounded overflow-hidden">
        <div class="progress-bar bg-blue-dark flex justify-center items-center text-white" role="progressbar" aria-valuenow="60" aria-valuemin="60" aria-valuemax="100"
          :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">{{ quoteCount }} / {{ maxQuotes }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quoteCount", "maxQuotes"]
};
</script>

<style scoped>
.progress-bar {
  transition: width .5s ease-in-out;
}
</style>