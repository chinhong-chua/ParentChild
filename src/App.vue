<template>
  <div id="app">
    <h1>Test parent child</h1>
    <button @click="showResults">Click me</button>
    <p v-if="show">{{ res }}</p>
    <Child @update="getResult" />
  </div>
</template>

<script>
import Child from "./components/child.vue";
export default {
  name: "App",
  components: { Child },
  data() {
    return {
      res: [],
      show: false,
    };
  },
  methods: {
    getResult(res) {
      this.res = res;
    },
    showResults() {
      this.show = !this.show;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
