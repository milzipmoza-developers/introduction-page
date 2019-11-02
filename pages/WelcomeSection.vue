<template>
  <div class="section">
    <div class="welcome-container">
      <div class="logo-layout">
        <img id="main-logo" class="main-logo main-logo-anim" src="../static/logo_transparent_bg.png"/>
      </div>
      <div class="title-layout">
        <div class="main-title">
          밀짚모자 개발단
        </div>
        <div class="sub-title">
          Milzipmoza Developers
        </div>
      </div>
      <div class="btn-layout">
        <a class="wrapper" href="https://github.com/milzipmoza-developers">
          <v-icon class="icon-btn icon-btn-anim icon-github-anim" color="#FFFFFF" large>fab fa-github</v-icon>
        </a>
        <a class="wrapper" href="https://www.youtube.com/channel/UCipvQqo32UmHkAAwhn-MfbQ">
          <v-icon class="icon-btn icon-btn-anim icon-youtube-anim" color="#FFFFFF" large>fab fa-youtube</v-icon>
        </a>
        <a class="wrapper" href="https://www.facebook.com/MilzipmozaDevelopers">
          <v-icon class="icon-btn icon-btn-anim icon-facebook-anim" color="#FFFFFF" large>fab fa-facebook</v-icon>
        </a>
        <a class="wrapper" href="https://instagram/thedevluffy">
          <v-icon class="icon-btn icon-btn-anim icon-instagram-anim" color="#FFFFFF" large>fab fa-instagram</v-icon>
        </a>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'Welcome',
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
    width: 350px;
    margin-top: 10vh;
    margin-bottom: 10vh;
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

  .btn-layout {
    margin-top: 50px;
    float: left;
    width: 100%;
    text-align: center;
  }

  .btn-layout > .wrapper {
    text-decoration: none;
    margin: 16px;
  }

  .icon-btn-anim:hover {
    padding-right: 12px;
    padding-left: 12px;
    font-size: 48px !important;
  }

  .icon-github-anim:hover {
    color: #2EFE2E !important;
  }

  .icon-youtube-anim:hover {
    color: #FE2E2E !important;
  }

  .icon-facebook-anim:hover {
    color: #2E64FE !important;
  }

  .icon-instagram-anim:hover {
    background: radial-gradient(circle at 33% 100%, #FED373 4%, #F15245 30%, #D92E7F 62%, #9B36B7 85%, #515ECF);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  @media ( max-width: 1023px ) {
    .logo-layout > .main-logo {
      width: 300px;
      margin-top: 10vh;
      margin-bottom: 10vh;
    }

    .title-layout > .main-title {
      font-family: 'Do Hyeon', sans-serif !important;
      font-size: 52px;
      letter-spacing: 5px;
      text-align: center;
      color: #ffffff !important;
    }

    .title-layout > .sub-title {
      font-family: 'Do Hyeon', sans-serif !important;
      font-size: 24px;
      text-align: center;
      color: #ffffff !important;
    }
  }

  @media ( max-width: 767px ) {
    .icon-github-anim {
      color: #2EFE2E !important;
    }

    .icon-youtube-anim {
      color: #FE2E2E !important;
    }

    .icon-facebook-anim {
      color: #2E64FE !important;
    }

    .icon-instagram-anim {
      background: radial-gradient(circle at 33% 100%, #FED373 4%, #F15245 30%, #D92E7F 62%, #9B36B7 85%, #515ECF);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  }
</style>

