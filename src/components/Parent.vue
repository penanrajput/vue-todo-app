<template>
  <div>
    <div v-if="val === 1">{{ val }} :Red</div>
    <div v-else-if="val === 2">{{ val }} : Green</div>
    <div v-else>{{ val }} : Other</div>
    <button v-on:click="add">+Add</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      val: 1,
    };
  },
  methods: {
    add() {
      this.val = this.val + 1;
    },
  },
};
</script>