<template>
  <div>
    <h1>AddTodo</h1>
    <input type="text" v-model="text">
    <button @click="add">Add</button>
  </div>
</template>

<script>
export default {
name: "AddTodo",

  data() {
  return {
    text: ''
  }
  },

  methods: {

    add()
    {
      this.$emit('addToDo', this.text)
    }
  }

}




</script>

<style scoped>

</style>
