<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
  export default {
    name: 'sticker-vue'
  }
</script>

<style>
  /* CSS */
  #app {
    height: 100%;
    width: 100%;
    position: fixed;
    overflow: hidden;
  }
</style>
