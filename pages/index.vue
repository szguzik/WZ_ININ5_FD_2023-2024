<script setup>
const open = ref(false)
const textButton = ref('Show modal')
const toggle = () => {
    open.value = !open.value
    textButton.value = open.value ? 'Hide modal' : 'Show modal'
}
</script>
<template>
    <h3>To jest strona główna</h3>
    <button @click="toggle">{{ textButton }}</button>
    <div v-if="open">To jest ukryty tekst</div>
</template>