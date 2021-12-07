<template>
    <form @submit.prevent='addTodo()'>
        <input type='text' v-model='newDescrip'>
        <button type='submit'>Añadir</button>
      </form>
</template>


<script>
export default {
  name: "add-todo",
  data() {
        return {
            newDescrip: '',
        }
    },
  methods: {
        addTodo() {
            this.$emit('despierta', {
                done: false,
                descrip: this.newDescrip,
            })
        }
    }
};
</script>

