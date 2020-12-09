<template>
    <div>
        <v-app-bar>
        <router-link to="/" class="nav-link"><v-btn class="nav-btn">Home</v-btn></router-link>
        <router-link to="/todo" class="nav-link"><v-btn class="nav-btn">TODO</v-btn></router-link>
        <router-link to="/about" class="nav-link"><v-btn class="nav-btn">About</v-btn></router-link>
        </v-app-bar>
        
    </div>
</template>

<script>

export default {
    
}
</script>

<style>
    .nav-btn {
        margin-left: 15px;
    }
    .nav-link {
        text-decoration: none;
    }
</style>