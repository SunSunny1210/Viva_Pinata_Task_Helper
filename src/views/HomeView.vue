<script setup>
</script>

<template>
  <div class="main">
    <div class="presentation">
      <img src="../assets/images/VivaPinataTIP.png" alt="Viva Piñata TP Logo">
      <button>Get Started!</button>
    </div>
    <div class="welcome">
      <h1>Welcome!</h1>
      <p class="description">This is Viva Piñata Task Planner, a website where you can keep record of your farm progress. Also, you can use it as a wiki, to check information about piñatas, plants, villagers and more!</p>
    </div>
  </div>
</template>

<style scoped>
  .main {
    height: 100vh;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: url(../assets/images/VPMain.png) no-repeat;
    background-size: 100% 100%;
    overflow-y: scroll;

    .presentation {
      padding: 1rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 2rem;
      background-color: rgba(255, 246, 246, 0.525);
      border-radius: 120px 120px;

      img {
        height: 30vh;
      }
  
      button {
        padding: 1rem;
        height: 10vh;
        width: 15vw;
        color: white;
        background-color: crimson;
        border: none;
        border-radius: var(--radius);
        font-size: var(--p-normal-size);
      }
    }

    .welcome {
      display: none;

      h1 {
        font-size: var(--h1);
      }

      p {
        font-size: var(--p-normal-size);
        text-align: center;
      }
    }
  }
</style>
