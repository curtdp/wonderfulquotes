<template>
  <div class="mx-auto block w-full max-w-md mb-4">
    <textarea v-model="quoteText" class="border rounded w-full mb-2" name="" id="" cols="30" rows="10"></textarea>
    <button @click="addQuote" class="block mx-auto border-blue-dark bg-blue text-white p-4 rounded hover:bg-blue-dark">Добавить цитату</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quoteText: ""
    };
  },
  methods: {
    addQuote() {
      this.$emit("addNewQuote", this.quoteText);
      this.quoteText = "";
    }
  }
};
</script>

<style scoped>
</style>