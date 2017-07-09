<template>
  <div class="one-home">
    <my-header></my-header>
    <banner></banner>
    <search></search>
    <section>
      <contentTitle></contentTitle>
      <my-summary></my-summary>
    </section>
  </div>
</template>
<script>
  import myHeader from './header/Header'
  import banner from './banner/banner'
  import search from './search/search'
  import contentTitle from './title/title'
  import mySummary from './summary/summary'

  export default {
    name: 'home',
    components: { myHeader, banner, search, contentTitle, mySummary }
  }
</script>
<style lang="postcss">
  @component-namespace one{
    @b home{
      width: 1200px;
    }
  }
</style>
