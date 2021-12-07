<template>
  <li>
    <input type="checkbox" checked="todo.done" />
    <span v-if="!todo.done">{{ todo.descrip }}</span>
    <del v-else>{{ todo.descrip }}</del>
  </li>
</template>


<script>
export default {
    name: 'todo-item',
    props: ['todo']
}
</script>