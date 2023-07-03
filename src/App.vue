<script setup lang="ts">
import {RouterLink, RouterView} from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import {ref} from "vue";

const title = ref<string>('My title')
const titleElement = ref();

function validate(event : Event) {
    (event.target as HTMLInputElement).blur()
    title.value = titleElement.value.innerText.trim()
}
defineExpose({ titleElement })
</script>

<template>
    <header>
        <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125"/>
        <div class="wrapper">
            <h1>I am title</h1>
            <p>added new commit</p>
            <nav>
                <RouterLink to="/">Option</RouterLink>
                <RouterLink to="/about">Setup</RouterLink>
                <RouterLink to="/service">Script setup</RouterLink>
            </nav>
            <h3>subtitle</h3>
        </div>
    </header>
    <HelloWorld msg="You did it!"/>
    <RouterView/>

    <template>
        <div ref="titleElement" contenteditable spellcheck="false" @blur="validate">
            {{ title }}
        </div>
    </template>
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
