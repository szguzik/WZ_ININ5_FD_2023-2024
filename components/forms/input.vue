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
    <input class="input is-primary" type="text" placeholder="Wprowadz text" v-model="valueDef">
</template>
<style scoped>

</style>