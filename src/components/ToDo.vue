<template>
  <div>
    <input
      v-model="text"
      placeholder="Enter your Task"
      v-on:keyup.enter="add"
    />
    <br />
    <br />
    <div>Current Task : {{ text }}</div>
    <br />

    <b-button @click="add">+Add</b-button>
    <br />
    <br />
    <h3 v-if="fruits.length > 0">Your Tasks:</h3>
    <ul>
      <ll
        v-for="(fruit, index) in fruits"
        :key="fruit.id"
        class="list-group-item d-flex justify-content-between"
      >
        {{ fruit }}
        <b-button variant="outline-success" @click="deleteElement(index)"
          >Done ✔</b-button
        >
      </ll>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "",
      fruits: [],
    };
  },
  methods: {
    add() {
      if (this.text) {
        this.fruits.push(this.text);
        this.text = "";
      }
    },
    deleteElement(id) {
      // this.fruits.delete(this.fruits.id);
      // alert("pressed deleete");
      // alert(id);

      this.fruits.splice(id, 1);
    },
  },
};
</script>

<style scoped>
</style>