<template>
  <div class="flex flex-wrap justify-between items-top">
    <div class="w-1/5 text-center" v-for="todo of todos" :key="todo.id">
      <a :href="todo.url">
        <img class="mx-auto" :src="todo.thumbnailUrl" alt="" />
        <p>{{ todo.title }}</p>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "fetchAPI",
  data() {
    return {
      errors: [],
      todos: [],
      urlTodos: "https://jsonplaceholder.cypress.io/photos?_limit=5",
    };
  },
  async mounted() {
    try {
      const takeData = await fetch(this.urlTodos);
      const result = await takeData.json();
      this.todos.push(...result);
      console.log(this.todos);
    } catch (error) {
      this.errors.push(error);
    }
  },
};
</script>
