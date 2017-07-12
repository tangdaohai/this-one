<template>
  <div class="one-summaryBH" :class="{big: size === 'big', small: size === 'small'}">
    <div class="one-summaryBH__list">
      <div class="one-summaryBH__card" v-for="card in summaryData" :key="card.unit">
        <img class="thumbnail" :src="card.src" alt="">

        <div v-if="overlap" class="one-summaryBH__description--overlap">
          <span class="unit">{{card.unit}}</span>
          <like :likeCount="card.likeCount"></like>
        </div>

        <div v-if="!overlap" class="one-summaryBH__description--nooverlap">
          <span class="text">{{card.text}}</span>
          <div>
            <span class="pubtime">{{card.time}}</span>
            <like :likeCount="card.likeCount"></like>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  /* 横向 大图 */
  import like from '../like/like'
  import './horizontal.css'

  export default{
    name: 'horizontal',
    components: { like },
    props: {
      summaryData: Array,
      size: String,
      overlap: Boolean
    }
  }
</script>
