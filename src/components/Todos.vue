<template>
  <div>
    <div v-for="todo in todos" v-bind:key="todo.id">
      <Item v-bind:todo='todo' v-on:del-todo="$emit('del-todo', todo.id)"/>
    </div>
  </div>
</template>

<script>
import Item from './Item.vue'
export default {
  name: "Todos",
  components: {
    Item
  },
  props: ["todos"]
}
</script>

<style scoped>
</style>
