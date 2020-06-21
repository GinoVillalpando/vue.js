<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
                <h1>{{ todo.title }}</h1>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Todos",
    props: ["todos"]
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