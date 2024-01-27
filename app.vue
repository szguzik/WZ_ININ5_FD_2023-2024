<script setup>
const openChat = ref(false)
const toggle = () => {
    openChat.value = !openChat.value
}
</script>
<template>
  <div>
  <NuxtLayout>
    <div class="body-content">
      <NuxtPage/>
    </div>
  </NuxtLayout>
  </div>
</template>
<style scoped>
  
</style>