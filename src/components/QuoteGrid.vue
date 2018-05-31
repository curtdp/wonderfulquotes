<template>
  <div class="flex -mx-4 flex-wrap">
    <Quote v-for="(quote, index) in quotes" :key="quote" @click.native="deleteQuote(index)">
      {{ quote }}
    </Quote>
  </div>
</template>

<script>
import Quote from "./Quote.vue";
export default {
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  },
  props: ["quotes"],
  components: {
    Quote
  }
};
</script>

<style scoped>
</style>