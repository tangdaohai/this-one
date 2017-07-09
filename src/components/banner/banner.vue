<template>
  <div class="one-banner">
    <div class="one-banner__slideshow">
      <img class="one-banner__slide" src="../../assets/banner01.jpg">
    </div>
    <div class="one-banner__indicator">
      <div v-for="i in 5" :key="i" :class="{isActive: i === 1}"></div>
    </div>
  </div>
</template>
<script>
  import './banner.css'
  export default{
    name: 'banner'
  }
</script>
