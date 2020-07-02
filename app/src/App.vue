<template>
  <v-app>
    <Header />
    <v-main>
      <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import Todos from './components/Todos.vue'
export default {
  name: 'App',
  components: {
    Header,
    Todos
  },
  data: () => ({
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
  }),
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
 * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background: #666;
  }
</style>