<template>
  <div class="one-summaryBH" :class="{big: size === 'big', small: size === 'small'}">
    <div class="one-summaryBH__list">
      <div class="one-summaryBH__card" v-for="card in summaryData" :key="card.unit">
        <img class="thumbnail" :src="card.src" alt="">
        <div class="one-summaryBH__description">
          <span class="unit">{{card.unit}}</span>
          <div class="like">
            <img class="icon" src="../../assets/unlike.png" alt="like">
            <span>({{card.likeCount}})</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  /* 横向 大图 */
  import './horizontal.css'
  export default{
    name: 'horizontal',
    props: {
      summaryData: Array,
      size: String
    }
  }
</script>
