<template>
  <div>
    <h1>{{ name }}</h1>
    <ul>
      <li v-for="item in items" :key="item.message">
        {{ item.message }}
      </li>
    </ul>
    <table>
      <tr>
        <td>ID</td>
        <td>NAME</td>
        <td>EMAIL</td>
      </tr>
      <tr v-for="contact in contacts" :key="contact.message">
        <td>{{ contact.id }}</td>
        <td>{{ contact.name }}</td>
        <td>{{ contact.email }}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "ListRendering",
  data() {
    return {
      name: "List Rendering",
      items: [{ message: "Foo" }, { message: "Bar" }],
      contacts: [
        { id: 1, name: "Penan", email: "penan@gmail.com" },
        { id: 2, name: "Foo", email: "foo@gmail.com" },
        { id: 3, name: "Bar", email: "bar@gmail.com" },
      ],
    };
  },
};
</script>

<style scoped>
li {
  text-align: left;
}
</style>