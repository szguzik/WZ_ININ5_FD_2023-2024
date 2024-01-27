<script setup>
const getData = (e) => {
    console.log('info z dziecka', e)
}
const fname = ref('')

onMounted(() => {
    setInterval(() => {
        fname.value =  localStorage.getItem('imie')
    }, 1000)
})
</script>
<template>
<h1>Hello</h1>
<h1>{{ fname }}</h1>
<FormsInput  
    :name="'Podaj imię'" 
    :valInput="''"  
    @sendValue="getData($event)"
/>
<FormsInput  
    :name="'Podaj Nazwisko'" 
    :valInput="''" 
    @sendValue="getData($event)"
/>
</template>
<style scoped lang="scss">

</style>