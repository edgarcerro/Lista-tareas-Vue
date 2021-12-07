<template>
  <h1>{{ title }}</h1>
  <todo-list :todos="todos"></todo-list>
  <add-todo @despierta="addTodo"></add-todo>
  <br>
  <delete-list @delall="deleteList"></delete-list>
</template>


<script>
import TodoList from "./components/TodoList.vue";
import AddTodo from "./components/AddTodo.vue";
import DeleteList from "./components/DeleteList.vue";

export default {
  name: "App",
  components: {
    TodoList,
    AddTodo,
    DeleteList,
    
  },
  data() {
    return {
      title: "Cosas a hacer",
      todos: [
        {
          id: 1,
          descrip: "Aprender Vue",
          done: false,
        },
        {
          id: 2,
          descrip: "Dominar Vue",
          done: false,
        },
      ],
    };
  },
  methods: {
        deleteList() {
            this.todos = []
        },
        
        addTodo(newTodo) {
            this.todos.push(newTodo)
        }
    }
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
