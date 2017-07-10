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

  * {
    font-family: '微软雅黑';
    margin: 0;
    padding: 0;
  }
</style>

