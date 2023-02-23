<script>
import OpenChild from "@/components/OpenChild.vue";

export default {
    components: {
        OpenChild
    },
    data() {
        return {
            message: '',
        }
    },
    methods: {
        concatFunc(msg) {
            this.message = msg;
        }
    },
}
</script>

<template>
    <main>
        <open-child :msg="'I am'" @concat="concatFunc"></open-child>
        <h1>Option API</h1>
        <p>{{ message }}</p>
    </main>
</template>
