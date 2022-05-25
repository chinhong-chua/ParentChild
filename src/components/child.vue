<template>
  <div>
    <h1>Child comp</h1>
  </div>
</template>

<script>
export default {
  data() {
    return { results: [1, 2, 3] };
  },
  mounted() {
    this.$emit("update", this.results);
  },
};
</script>

<style></style>
