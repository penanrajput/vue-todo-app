<template>
  <div>
    <ul>
      <li v-for="fruit in fruits" :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fruits: ["apples", "mango", "grapes"],
    };
  },
};
</script>