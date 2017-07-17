<template>
  <div class="one-banner">
    <div class="one-banner__slideshow">
      <transition name="switch" mode="out-in">
        <img class="one-banner__slide"
          :src="bannerArr[current % bannerArr.length]"
          :key="bannerArr[current % bannerArr.length]"
          @mouseenter="mouseenter"
          @mouseleave="mouseleave">
      </transition>
    </div>
    <div class="one-banner__indicator">
      <div v-for="i in 5"
        :key="i"
        :class="{isActive: i === (current % bannerArr.length + 1)}"
        @click="switchBanner(i - 1)"
        @mouseenter="mouseenter"
        @mouseleave="mouseleave">
      </div>
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
        loopState: true,
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
      },
      mouseenter () {
        this.loopState = false
      },
      mouseleave () {
        this.loopState = true
      }
    },
    created () {
      setInterval(() => {
        this.loopState && this.current++
      }, 3000)
    }
  }
</script>
