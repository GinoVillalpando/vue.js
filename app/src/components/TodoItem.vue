<template>
    <div>
        <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
            <p>
                <input type="checkbox" v-on:change="Complete">
                {{ todo.title }}
            </p>

        </div>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        Complete() {
            this.todo.completed = !this.todo.completed;
            console.log(this.todo.completed)
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