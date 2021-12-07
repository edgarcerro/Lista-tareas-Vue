<template>
  <ul>
    <todo-item
      v-for="(todo, index) in todos"
      :key="index"
      :todo="todo"
    ></todo-item>
  </ul>
</template>


<script>
import TodoItem from './TodoItem.vue';

export default {
  components: { TodoItem },
  name: "todo-list",
  props: ['todos']
};
</script>

