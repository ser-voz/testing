<script>
export default {
    name: "SetupChild",
    emits: ['concat'],
    props: {
        msg: String,
    },
    setup(props, { emit }) {
        emit("concat", props.msg + ' child setup');
    },
}
</script>

<template>
    <div></div>
</template>

<style scoped>

</style>