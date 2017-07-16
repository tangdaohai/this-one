<template>
  <div class="one-banner">
    <div class="one-banner__slideshow">
      <transition name="switch" :duration="{ leave: 400 }">
        <img class="one-banner__slide" :src="bannerArr[current % 5]" :key="bannerArr[current % 5]">
        <!-- <img class="one-banner__slide is-seccend" :src="bannerArr[current % 5 + 1]" :style="{ order: 1 }"> -->
      </transition>
    </div>
    <div class="one-banner__indicator">
      <div v-for="i in 5" :key="i" :class="{isActive: i === (current % 5 + 1)}" @click="switchBanner(i - 1)"></div>
    </div>
  </div>
</template>
<script>
  import './banner.css'
  export default {
    name: 'banner',
    data () {
      return {
        current: 0,
        bannerArr: [
          require('../../assets/banner01.jpg'),
          require('../../assets/banner02.jpg'),
          require('../../assets/banner03.jpg'),
          require('../../assets/banner04.jpg'),
          require('../../assets/banner05.jpg')
        ]
      }
    },
    methods: {
      switchBanner (index) {
        this.current = index
      }
    },
    created () {
      setInterval(() => {
        this.current++
      }, 2000)
    }
  }
</script>
