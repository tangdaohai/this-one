<template>
  <div class="one-home">
    <my-header></my-header>
    <banner></banner>
    <search></search>
    <section>
      <!-- 期刊 -->
      <contentTitle title="期刊" :types="['放松', '安静', '治愈', '浪漫']"></contentTitle>
      <my-summary :summaryData="summaryData" direction="h" size="big"></my-summary>
      <my-summary :summaryData="summaryDataSmall" direction="h" size="small"></my-summary>

      <contentTitle title="单曲" :types="['后摇', '民谣', '流行', '独立音乐']"></contentTitle>
    </section>
  </div>
</template>
<script>
import myHeader from './header/Header'
import banner from './banner/Banner'
import search from './search/Search'
import contentTitle from './title/Title'
import mySummary from './summary/Summary'

export default {
  name: 'home',
  components: { myHeader, banner, search, contentTitle, mySummary },
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
