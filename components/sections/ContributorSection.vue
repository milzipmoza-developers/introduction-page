<template>
  <div class="section">
    <div class="contributor-container">
      <div class="contributor-title">
        Members
      </div>
      <div style="color: white">
        준비중...
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Contributor',
    data: () => ({})
  }
</script>

<style>
  .contributor-container {
    background-color: black;
    height: 100%;
    width: auto;
    padding: 3vh;
    padding-right: 20vw !important;
    padding-left: 20vw !important;
  }

  .contributor-title {
    margin-bottom: 24px;
    font-size: 64px;
    color: white;
    font-family: 'Noto Sans KR', sans-serif;
    font-weight: bold;
  }

  @media ( max-width: 1488px ) {
    .contributor-container {
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
    }
  }

  @media ( max-width: 767px ) {
  }
</style>

