<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoItem v-bind:todo="todo"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {

    name: "Todos",
    components: {
        TodoItem
    },
    props: ["todos"],
    methods: {
        Complete() {
            this.todos.completed = !this.todos.completed;
            console.log(this.todos)
        }
    }
}
</script>

<style scoped>
    .todo-item {
        background: #333;
        padding: 2rem;
        border-bottom: 1px black dashed;
    }
    .is-complete {
        text-decoration: line-through;
    }

</style>