<template>
  <div id="app">
    <HelloWorld msg="To-Do App" about="this app will list things you have to do. You'll be able to mark them as completed or imcomplete and delete them or add them."/>
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Todos
  },
  data() {
    return{
      todos: [
        {
          id: 1,
          title: "wash the car",
          completed: false
        },
        {
          id: 2,
          title: "wash the dishes",
          completed: false
        },
        {
          id: 3,
          title: "walk cloudadawa",
          completed: false
        }
        ]
    }
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(
        todo => todo.id !== id
      )
    }
  }
}
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
