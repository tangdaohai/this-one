<template>
  <div class="one-home">
    <my-header></my-header>
    <banner></banner>
    <search></search>
    <section>
      <!-- 期刊 -->
      <contentTitle title="期刊" :types="['放松', '安静', '治愈', '浪漫']"></contentTitle>
      <my-summary :summaryData="summaryData" overlap direction="h" size="big"></my-summary>
      <my-summary :summaryData="summaryDataSmall" overlap direction="h" size="small"></my-summary>
      <!-- 单曲 -->
      <contentTitle title="单曲" :types="['后摇', '民谣', '流行', '独立音乐']"></contentTitle>
      <single-music></single-music>
      <my-summary :summaryData="summaryDataNoOverlap" direction="h" size="small"></my-summary>

      <contentTitle title="一段故事"></contentTitle>
    </section>
  </div>
</template>
<script>
import myHeader from './header/Header'
import banner from './banner/Banner'
import search from './search/Search'
import contentTitle from './title/Title'
import mySummary from './summary/Summary'
import singleMusic from './single-music/single-music'

export default {
  name: 'home',
  components: { myHeader, banner, search, contentTitle, mySummary, singleMusic },
  data () {
    return {
      summaryData: [
        {
          src: require('../assets/56e04233bae99.jpg'),
          unit: '第五期',
          likeCount: 192
        }, {
          src: require('../assets/56e04233bae99.jpg'),
          unit: '第四期',
          likeCount: 192
        }
      ],
      summaryDataSmall: [
        {
          src: require('../assets/56e04233bae99.jpg'),
          unit: '第三期',
          likeCount: 192
        }, {
          src: require('../assets/56e04233bae99.jpg'),
          unit: '第二期',
          likeCount: 192
        }, {
          src: require('../assets/56e04233bae99.jpg'),
          unit: '第一期',
          likeCount: 192
        }
      ],
      summaryDataNoOverlap: [
        {
          src: require('../assets/m_58b92358cd339.jpg'),
          text: 'Alcest: 生命犹如一趟从明亮到黑暗的旅程',
          time: '2017.03.23',
          likeCount: 177
        }, {
          src: require('../assets/m_58982d024420b.jpg'),
          text: '让风雨归我，孤寂归我',
          time: '2017.03.23',
          likeCount: 177
        }, {
          src: require('../assets/m_58258a6fe7547.jpg'),
          text: 'Alcest: 生命犹如一趟从明亮到黑暗的旅程',
          time: '2017.03.23',
          likeCount: 177
        }
      ]
    }
  }
}
</script>
<style lang="postcss">
  @component-namespace one{
    @b home{
      width: 1200px;
    }
  }
</style>
