


<template>
  <div id="app">
      <TodoList :todos="todos" @delete-todo="deleteTodo"/>
  </div>
</template>

<script>
 import TodoList from "@/components/TodoList";
  export default{
    name: 'app',
    data(){
      return{
         todos: ['ремонт', 'завтрак', 'hello!' ]
      }
    },
    methods: {
      deleteTodo(index){
        this.todos.splice(index,1)
      }
    },
    components: {
      TodoList
    }
  }
</script>

<style>

</style>
