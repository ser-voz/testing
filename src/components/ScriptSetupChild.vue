<script setup>
const emit = defineEmits(['concat'])
const props = defineProps({msg: String})
emit('concat', props.msg + ' child script setup');
</script>

<template>
    <div></div>
</template>

<style scoped>

</style>