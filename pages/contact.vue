<script setup>
const getData = (e) => {
    console.log('info z dziecka', e)
}
</script>
<template>
<h1>contact</h1>
<FormsInput  :name="'Podaj imię'" :valInput="''"  @sendValue="getData($event)"/>
<FormsInput  :name="'Podaj Nazwisko'" :valInput="''"  @sendValue="getData($event)"/>
</template>
<style scoped lang="scss">

</style>