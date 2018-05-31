<template>
<div>
  <div class="container mx-auto">
    <Header :maxQuotes="maxQuotes" :quoteCount="quotes.length"></Header>
  </div>
  <div class="container mx-auto">
    <new-quote @quoteAdded="newQuote"></new-quote>
  </div>
  <div class="container mx-auto">
    <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
  </div>
  <div class="container mx-auto">
    <div class="p-4 text-center rounded border border-red-dark bg-red-lighter">Кликните по цитате для удаления</div>
  </div>
</div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import Header from "./components/Header.vue";
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
  components: {
    Header,
    QuoteGrid,
    NewQuote
  }
};
</script>

<style src="./assets/styles/main.css"></style>
