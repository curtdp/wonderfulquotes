<template>
  <div class="w-full  flex-wrap sm:w-1/2 md:w-1/3 lg:w-1/4 xl:w-1/6 quote-wrapper">
    <div class="p-4 m-4 border border-grey rounded shadow-md overflow-hidden bg-white quote">
      <slot></slot>
    </div>
  </div>
</template>

<script>
</script>

<style scoped>
.quote-wrapper {
  font-family: "Marck Script", cursive;
  font-size: 2rem;
  color: #6e6e6e;
}
.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
}
</style>