<template>
<form>
  <div class="w-full border rounded shadow-md border-grey bg-white mt-8 sm:w-1/1 md:w-1/2 mx-auto mb-4 quote-wrapper">
    <div class="p-4 flex flex-col">
      <label class="my-2" for="quote">Цитата</label>
      <textarea id="quote" cols="30" rows="3" v-model="quote" class="border border-grey-dark rounded"></textarea>
    </div>
    <div class="border-b border-grey-light p-4 text-center">
      <button class="bg-blue active:bg-blue-dark text-white font-semibold hover:text-white py-2 px-4 rounded" @click.prevent="createNew">Добавить цитату</button>
    </div>
  </div>
</form>
</template>

<script>
export default {
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      if (this.quote !== "") {
        this.$emit("quoteAdded", this.quote);
        this.quote = "";
      }
    }
  }
};
</script>

<style scoped>
</style>