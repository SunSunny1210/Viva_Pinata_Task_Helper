<script setup>
</script>

<template>
  <div class="background"></div>
  <div class="filter"></div>
  <div class="body">
    <RouterView></RouterView>
  </div>
</template>

<style scoped>
  .body {
    display: flex;
    justify-content: center;
    align-items: center;

  }

  .background {
    position: fixed;
    height: 100vh;
    width: 100vw;
    background: url(./assets/images/background.jpg);
    filter: blur(2px);
    z-index: -2;
  }

  .filter {
    position: fixed;
    height: 100vh;
    width: 100vw;
    background-color: rgba(255, 247, 195, 0.345);
    z-index: -1;
  }
</style>
