<script setup>
const props = defineProps({
    valInput: {
        type: String,
        default: ''
    },
    name: {
        type: String,
        default: ''
    }
})

const emit = defineEmits(['sendValue'])

const valueDef = ref(props.valInput)

watch(valueDef, (newVal, oldVal) => {
    console.log(newVal, oldVal)
    emit('sendValue', newVal)
})





</script>
<template>
    {{ name }}
    <input v-model="valueDef"><br>
</template>
<style scoped>

</style>