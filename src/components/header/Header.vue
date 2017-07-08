<template>
  <div class="one-header">
    <img class="one-header__logo" src="../..//assets/logo.png"></img>
    <div class="one-header__menu">
      <div v-for="menu in menuArray" :key="menu">{{menu}}</div>
    </div>
  </div>
</template>
<script>
import './header.css'

export default {
  name: 'my-header',
  data () {
    return {
      menuArray: ['期刊', '单曲', '故事', '老照片']
    }
  }
}
</script>
