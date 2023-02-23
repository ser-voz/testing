<script setup lang="ts">
import {RouterLink, RouterView} from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
    <header>
        <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125"/>
        <div class="wrapper">
            <nav>
                <RouterLink to="/">Option</RouterLink>
                <RouterLink to="/about">Setup</RouterLink>
                <RouterLink to="/service">Script setup</RouterLink>
            </nav>
        </div>
    </header>
    <HelloWorld msg="You did it!"/>

    <RouterView/>
</template>

<style scoped>
header {
    text-align: center;
    margin-bottom: 50px;
}

nav a {
    margin: 0 10px;
    font-size: 18px;
}
</style>
