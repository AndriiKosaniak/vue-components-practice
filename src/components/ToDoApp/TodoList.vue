<template>
  <div>
    <h1>TodoList</h1>
    <ul>
      <li v-for="(todo, i) in toDoList" :key="i">
        {{todo}}
        <TodoItem :todo="todo"
        @addToDo="addToDo"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";

export default {
  name: "TodoList",

  props: {
    toDoList: {
      type: Array,
      required: true
    }
  },
  components: {
    TodoItem
  },
  methods: {
    addToDo(){
      this.toDoList.push(this.text)
    }
  }
}
</script>

<style scoped>

</style>
