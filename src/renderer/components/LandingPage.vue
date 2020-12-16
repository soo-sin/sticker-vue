<template>

  <textarea id="note">
  </textarea>
</template>

<script>
  export default {
    name: 'landing-page',
    components: { },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    /*box-sizing: border-box;*/
    margin: 0;
    padding: 0;
  }

  body {
    font-family: 'Source Sans Pro', sans-serif;
    height: 100vh;
    width: 100vw;
    max-width: 100%;
    max-height: 100%;
  }

  #note {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    resize: none;
    font-size: 30px;
  }

</style>
