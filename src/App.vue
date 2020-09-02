<template>
  <div>
  <TodoList :toDoList="toDoList"></TodoList>
    <AddTodo/>
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
      toDoList: [
        {
          action: 'WakeUp',
          priority: 'high'
        },
        {
          action: 'BrushTeeth',
          priority: 'high'
        },
        {
          action: 'HaveBreakfast',
          priority: 'medium'
        },
        {
          action: 'Reading',
          priority: 'low'
        }
      ]
    }
  },

}
</script>

<style>

</style>
