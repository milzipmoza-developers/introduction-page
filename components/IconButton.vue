<template>
  <a class="wrapper" target="_blank" rel="noopener noreferrer" :href="href">
    <v-icon class="icon-btn" :color="color" large>{{ icon }}</v-icon>
  </a>
</template>

<script>
export default {
  props: {
    href: {
      type: String
    },
    icon: {
      type: String
    },
    color: {
      type: String
    }
  }
}
</script>

<style>
  .wrapper {
    text-decoration: none;
    margin: 8px;
  }
</style>
