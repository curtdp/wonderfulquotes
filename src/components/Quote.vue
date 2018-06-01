<template>
  <div class="px-2 w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 mb-4">
    <div class="quote text-2xl border rounded bg-white hover:bg-red-lighter shadow-md p-4 cursor-pointer">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.quote {
  font-family: "Marck Script", cursive;
}
</style>