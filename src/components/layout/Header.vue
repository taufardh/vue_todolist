<template>
    <header class="header">
        <div class="container">
            <nav class="navbar navbar-dark bg-dark">
                <!-- Navbar content -->
                <span class="navbar-brand mb-0 h1">TodoList App.</span>
                <form class="form-inline">
                    <button class="btn btn-outline-success" type="button"> <router-link to="/">Home</router-link></button>
                    <button class="btn btn-outline-success" type="button"><router-link to="/about">About</router-link></button>
                </form>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    .header {
        color: #fff;
    }

    .header a {
        color: #fff;
        padding-right: 5px;
        text-decoration: none;
    }
    
</style>