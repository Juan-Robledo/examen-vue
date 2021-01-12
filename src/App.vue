<template>
  <div>
    <home></home>
  </div>
</template>

<script>

import Home from './views/Home.vue'
export default {
  components: { Home },
  name: 'App',
}
</script>

<style>
  body{
    width: 280px;
    height: 529px;
    border: 1px solid #333333;
    padding: 15px;
  }
  ul{
    width: 80%;
    padding: 0;
    margin: 10px auto;
    border: 1px solid #333333;
    display: flex;
    justify-content: space-between;
  }
  li{
    list-style: none;
  }
</style>
