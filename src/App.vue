<template>
  <div>
  <TodoList :toDoList="toDoList"></TodoList>
    <AddTodo
    @addToDo="addToDo"
    />
  </div>
</template>

<script>

import TodoList from "./components/ToDoApp/TodoList";
import AddTodo from "./components/AddTodo";

export default {
  name: 'App',



  components: {
    TodoList,
    AddTodo
  },

  data() {
    return {
      toDoList: []
    }
  },

  methods: {
    addToDo() {
      this.toDoList.push(this.text)
    },
  }
}
</script>

<style>

</style>
