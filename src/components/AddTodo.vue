<template>
  <div>
    <h1>AddTodo</h1>
    <input type="text" v-model="text">
    <button @click="addToDo">Add</button>
  </div>
</template>

<script>
export default {
name: "AddTodo",

  methods: {
    addToDo() {
      this.toDoList.push(this.text)
    },


    add()
    {
      this.$emit('addToDo', this.text)
    }
  }

}




</script>

<style scoped>

</style>