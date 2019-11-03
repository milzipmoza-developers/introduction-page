<template>
  <a class="wrapper" target="_blank" rel="noopener noreferrer" :href="href">
    <img class="img-icon" src="../static/tecobrary_white_logo.png" alt="github-btn">
  </a>
</template>

<script>
  export default {
    name: "ImageButton.vue",
    props: {
      src: {
        type: String
      },
      href: {
        type: String
      }
    }
  }
</script>

<style scoped>
  .img-icon {
    width: 35px;
    height: 35px;
    /* v-icon css attributes */
    -webkit-box-align: center;
    align-items: center;
    display: inline-flex;
    font-feature-settings: "liga";
    -webkit-box-pack: center;
    justify-content: center;
    letter-spacing: normal;
    line-height: 1;
    text-indent: 0;
    -webkit-transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1);
    transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1);
    vertical-align: middle;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  .wrapper {
    text-decoration: none;
    margin: 8px;
  }
</style>
