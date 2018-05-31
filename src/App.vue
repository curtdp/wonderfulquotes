<template>
  <div class="container mx-auto">
    <h1>Hello</h1>
  </div>
  <div class="container mx-auto">
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
export default {
  data() {
    return {
      maxQuotes: 10,
      quotes: ["Просто цитата чтобы что-то увидеть"]
    };
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  name: "app",
  components: {}
  components: {
    QuoteGrid,
  }
};
</script>

<style src="./assets/styles/main.css"></style>
