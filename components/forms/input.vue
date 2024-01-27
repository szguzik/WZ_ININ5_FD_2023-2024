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

const saveInlStorage = () => {
    localStorage.setItem('imie', valueDef.value)
}

const removeFromlStorage = () => {
    localStorage.removeItem('imie')
}
</script>
<template>
    {{ name }}
    <input 
        class="input is-primary" 
        type="text" 
        placeholder="Wprowadz text" 
        v-model="valueDef"
    >

    <button type="button" class="button is-primary" @click="saveInlStorage">Zapisz</button>
    <button type="button" class="button is-primary" @click="removeFromlStorage">Usun</button>

</template>
<style scoped>

</style>