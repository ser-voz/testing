<script>
import SetupChild from "@/components/SetupChild.vue";
import {ref} from "vue";

export default {
    components: {SetupChild},
    setup() {
        const message = ref('');
        const concatFunc = (msg) => {
            message.value = msg;
        }
        return {
            message,
            concatFunc
        }
    },
}
</script>

<template>
    <main>
        <setup-child :msg="'I am'" @concat="concatFunc"></setup-child>
        <h1>Setup</h1>
        {{ message }}
    </main>
</template>

<style>

</style>
