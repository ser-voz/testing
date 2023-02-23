<script setup lang="ts">
import ScriptSetupChild from "@/components/ScriptSetupChild.vue";
import {ref} from "vue";

const message = ref('');

const concatFunc = (msg: string) => {
    message.value = msg;
}
</script>

<template>
    <main>
        <ScriptSetupChild :msg="'I am'" @concat="concatFunc"/>
        <h1>Script Setup</h1>
        {{ message }}
    </main>
</template>

<style scoped>

</style>