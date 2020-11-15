<template>
  <div>
    Enter the email
    <h1>{{ email }}</h1>
    <br />
    <input type="text" v-model="email" :class="{ red: email.length < 2 }" />
    <br />
    <br />
    <input
      type="text"
      v-model="email"
      :class="[email.length < 2 ? 'red' : 'green']"
    />
    <br />

    <button @click="msg" :disabled="email.length < 2">Submit</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: "",
    };
  },
  methods: {
    msg() {
      alert("done");
    },
  },
  filter: {
    username: function (value) {
      return value.toUpperCase();
    },
  },
};
</script>

<style scoped>
.red {
  border: 2px solid red;
}
.green {
  border: 2px solid green;
}
</style>