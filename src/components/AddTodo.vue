<template>
    <div class="container mb-5">
        <form class="form-signin" @submit.prevent="addTodo">
            <div class="text-center mb-4">
                <h1 class="h3 mb-3 font-weight-normal">Floating labels</h1>
            </div>
            <div class="form-label-group">
                <input type="text" class="form-control" v-model="title" name="title" placeholder="Add Todo..." required autofocus>
                <label for="inputAddTodo"><br></label>
            </div>
            <button class="btn btn-primary" type="submit">Submit</button>
        </form>
    </div>
</template>

<script>
//import uuid from 'uuid';

export default {
    name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addTodo() {
            const newTodo = {

                title: this.title,
                completed: false
            }
            //Send up to partent
            this.$emit('add-todo', newTodo);

            this.title = '';
        }
    }
}
</script>

<style scoped>
    
</style>