<template>
  <div class="section">
    <div class="welcome-container">
      <div class="logo-layout">
        <img id="main-logo" class="main-logo" src="../static/main_logo.png" @onmouseover="mainLogoMouseOver"/>
      </div>
      <div class="title-layout">
        <div class="main-title">
          밀짚모자 개발단
        </div>
        <div class="sub-title">
          Milzipmoza Developers
        </div>
      </div>
      <div class="button-layout">
        <!-- 깃헙, 유튜브, 페이스북 페이지, 인스타그램 -->
        <v-icon class="icon-button" color="#FFFFFF" large>fab fa-github</v-icon>
        <v-icon class="icon-button" color="#FFFFFF" large>fab fa-youtube</v-icon>
        <v-icon class="icon-button" color="#FFFFFF" large>fab fa-facebook</v-icon>
        <v-icon class="icon-button" color="#FFFFFF" large>fab fa-instagram</v-icon>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'Welcome',

    data: () => ({
      dd: 1
    }),

    methods: {
      mainLogoMouseOver: function () {
        const mainLogo = document.getElementById("main-logo")
        console.log('dd')
      }
    }
  }
</script>

<style>
  .welcome-container {
    background-color: black;
    height: 100%;
    width: auto;
    padding-top: 10vh;
  }

  .logo-layout {
    text-align: center;
    vertical-align: center;
  }

  .logo-layout > .main-logo {
    width: 50%;
  }

  .title-layout {
    align-items: center;
  }

  .title-layout > .main-title {
    font-family: 'Do Hyeon', sans-serif !important;
    font-size: 60px;
    letter-spacing: 5px;
    text-align: center;
    color: #ffffff !important;
  }

  .title-layout > .sub-title {
    font-family: 'Do Hyeon', sans-serif !important;
    font-size: 32px;
    text-align: center;
    color: #ffffff !important;
  }

  .button-layout {
    margin-top: 50px;
    float: left;
    width: 100%;
    text-align: center;
  }

  .button-layout > .icon-button {
    padding: 16px;
  }

  @media ( max-width: 1023px ) {

  }

  @media ( max-width: 767px ) {

  }
</style>

