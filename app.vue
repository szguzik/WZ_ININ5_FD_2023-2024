<template>
  <div>
  <NuxtLayout>
    <div class="body-content">
      <NuxtPage/>
    </div>
  </NuxtLayout>
  <div class="circle"></div>
  </div>
</template>
<style scoped>
  .circle {
    width: 50px;
    height: 50px;
    background-color: #3498db; /* Kolor tła */
    border-radius: 50%; /* Ustala kształt koła */
    position: absolute; /* Pozycja absolutna */
    bottom: 0; /* Odległość od dołu */
    right: 0; /* Odległość od prawej */
  }
</style>