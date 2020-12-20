<template>
  <textarea v-model="memoContent" @keyup="saveContent" id="note"/>
</template>

<script>
  export default {
    name: 'landing-page',
    data: () => {
      return {
        memoContent: ''
      }
    },
    components: {

    },
    // 화살표함수를 쓰면 this를 가져가므로 주의
    created () {
      this.memoContent = localStorage.getItem('memoContent')
    },
    methods: {
      saveContent () {
        localStorage.setItem('memoContent', this.memoContent)
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    margin: 0;
    padding: 0;
  }

  html {
    width: 100%;
    height: 100%;
  }

  body {
    font-family: 'Source Sans Pro', sans-serif;
    height: 100%;
    width: 100%;
    max-width: 100%;
    max-height: 100%;
  }

  #note {
    width: 100%;
    height: 100%;
    border: none;
    outline: none;
    resize: none;
    font-size: 16px;
    background-color: #FFFBD3;
    padding: 16px;
  }

</style>
