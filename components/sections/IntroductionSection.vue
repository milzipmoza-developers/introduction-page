<template>
  <div class="section">
    <div class="contributor-container">
      <div class="contributor-title">
        Introduction
      </div>
      <div style="color: white">
        준비중...
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Introduction',
    data: () => ({
    })
  }
</script>

<style>
  .contributor-container {
    margin-top: 40px;
    background-color: black;
    height: 100%;
    width: auto;
    padding: 36px;
    padding-right: 20vw !important;
    padding-left: 20vw !important;
  }

  .contributor-title {
    margin-bottom: 24px;
    font-size: 70px;
    color: white;
    font-family: 'Do Hyeon', sans-serif !important;
  }

  @media ( max-width: 1488px ) {
    .contributor-container {
      margin-top: 30px;
      background-color: black;
      height: 100%;
      width: auto;
      padding: 36px;
      padding-right: 15vw !important;
      padding-left: 15vw !important;
    }
  }

  @media ( max-width: 1279px ) {
    .contributor-container {
      margin-top: 20px;
      background-color: black;
      height: 100%;
      width: auto;
      padding: 36px;
      padding-right: 10vw !important;
      padding-left: 10vw !important;
    }
  }

  @media ( max-width: 1023px ) {
    .contributor-container {
      margin-top: 20px;
      background-color: black;
      height: 100%;
      width: auto;
      padding: 36px;
      padding-right: 7vw !important;
      padding-left: 7vw !important;
    }

    .contributor-title {
      margin-bottom: 24px;
      font-size: 50px;
      color: white;
      font-family: 'Do Hyeon', sans-serif !important;
    }
  }

  @media ( max-width: 767px ) {
  }
</style>

