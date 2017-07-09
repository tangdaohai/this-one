<template>
  <div class="one-header">
    <img class="one-header__logo" src="../..//assets/logo.png"></img>
    <div class="one-header__menus">
      <div class="one-header__menu" v-for="menu in menuArray" :key="menu">
        <span>{{menu}}</span>
      </div>
    </div>
    <div class="one-header__user">注册/登录</div>
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
