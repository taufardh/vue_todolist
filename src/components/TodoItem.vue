<template>
    <div v-bind:class="['list-group-item', (todo.completed === true ? 'list-group-item-action' : 'list-group-item-success'), (todo.completed === false ? 'list-group-item-action' : 'list-group-item-danger')]">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}}
            <button @click="$emit('del-todo', todo.id)" class="del btn btn-danger">x</button>
        </p>
    </div>
</template>

<script>
export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
        markComplete(){
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>


    .is-complete {
        text-decoration: line-through;
    }

    .del {
        cursor: pointer;
        float: right;
    }
</style>