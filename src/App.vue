<template>
  <div id="app">
    <!-- <ConditionalRendering /> -->
    <!-- <ListRendering /> -->
    <!-- <Parent /> -->
    <!-- <Child /> -->
    <ToDo/>
  </div>
</template>

<script>
// import ConditionalRendering from "./components/ConditionalRendering.vue";
// import ListRendering from "./components/ListRendering";
// import Child from "./components/Child";
// import Parent from "./components/Parent";
import ToDo from './components/ToDo'
export default {
  name: "App",
  components: {
    // ConditionalRendering,
    // ListRendering,
    // Parent,
    // Child,
    ToDo

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
