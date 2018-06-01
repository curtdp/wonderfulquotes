<template>
  <div class="container w-5/6 mx-auto mt-8">
    <div>
      <h1 class="mb-4">Цитаты</h1>
      <progress-bar :maxQuotes="maxQuotes" :quotesCount="quotes.length" />
    </div>
    <div class="border-b mb-4">
      <new-quote @addNewQuote="newQuote" />
    </div>
    <div class="mb-4">
      <quote-grid @quoteDeleted="deleteQuote" :quotes="quotes"></quote-grid>
    </div>
    <div class="text-center bg-red-lighter p-2 rounded border border-red">Кликните по цитате чтобы удалить ее</div>
  </div>
</template>

<script>
import ProgressBar from "./components/ProgressBar.vue";
import NewQuote from "./components/NewQuote.vue";
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
      if (this.quotes.length >= 10) {
        return alert("Удалите цитату");
      }
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  },
  name: "app",
  components: {
    ProgressBar,
    NewQuote,
    QuoteGrid
  }
};
</script>

<style src="./assets/styles/main.css"></style>
