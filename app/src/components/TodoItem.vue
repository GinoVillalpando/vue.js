<template>
    <div>
        <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
            <input type="checkbox" v-on:change="Complete">
                 <p>{{ todo.title }}</p>
            <button @click="$emit('del-todo', todo.id)" class="del">x</button>
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
        margin-left: 2rem;
        margin-right: 2rem;
        border-bottom: 1px black dashed;
        display: flex;
        justify-content: space-between;
    }
    .is-complete {
        text-decoration: line-through;
    }
    .del {
    background: #ff0000;
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
  }

</style>