<script>
export default {
    name: "OpenChild",
    props: {
        msg: String
    },
    methods: {
        concatString() {
            this.$emit('concat', this.$props.msg + ' child option');
        }
    },
    mounted() {
        this.concatString();
    }
}
</script>

<template>

</template>


<style scoped>

</style>