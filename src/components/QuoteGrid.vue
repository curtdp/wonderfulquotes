<template>
  <div class="flex flex-wrap -m-2">
    <Quote @click.native="deleteQuote(index)" v-for="(quote, index) in quotes" :key="index">
      {{ quote }}
    </Quote>
  </div>
</template>

<script>
import Quote from "./Quote.vue";
export default {
  props: ["quotes"],
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  },
  components: {
    Quote
  }
};
</script>

<style scoped>
</style>