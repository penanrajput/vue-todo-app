<template>
  <div>
    <h1>hello {{ title }}</h1>
    <h1 v-if="awesome">Vue is awesome</h1>
    <h1 v-else>Vue is cool</h1>
    <button v-on:click="toggle()">Toggle H2 Tag</button>
    <br /><br />
    <div v-if="type === 'A'">A</div>
    <div v-else-if="type === 'B'">B</div>
    <div v-else-if="type === 'C'">C</div>
    <div v-else>Not A/B/C</div>
  </div>
</template>

<script>
export default {
  name: "ConditionalRendering",
  data() {
    return {
      title: "ConditionalRendering",
      awesome: false,
      type: "A",
    };
  },
  methods: {
    toggle() {
      this.awesome = !this.awesome;
      // alert(this.awesome);
    },
  },
};
</script>