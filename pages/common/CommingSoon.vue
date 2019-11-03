<template>
  <div class="luffy-container">
    Comming Soon
  </div>
</template>

<script>
  export default {
    name: "CommingSoon.vue",
    beforeCreate() {
      console.log('디벨로핑 메리호 건조중')
      console.log('[■■■☐☐☐☐☐☐☐] 30%')
    }
  }
</script>

<style scoped>
  .luffy-container {
    height: 100vh;
    text-align: center;
    padding-top: 100px;
    font-size: 45px;
    color: white;
    background-color: black;
    font-family: 'Do Hyeon', sans-serif !important;
  }
</style>
