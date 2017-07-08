<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>
<style>
  #app{
    display: flex;
    justify-content: center;
  }

  /* body 样式*/
  body {
    font-family: '微软雅黑'
  }
</style>

