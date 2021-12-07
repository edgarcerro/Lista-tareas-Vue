<template>
  <button @click="borrarTodos">Borrar toda la lista</button>
</template>


<script>
export default {
  name: "delete-list",
  methods: {
        borrarTodos() {
            if (confirm('Vas a borrar toda la lista')) {
                this.$emit('delall')
            }
        }
    }
};
</script>

