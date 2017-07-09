<template>
  <div class="one-home">
    <my-header></my-header>
    <banner></banner>
    <search></search>
    <section>
      <contentTitle></contentTitle>
    </section>
  </div>
</template>
<script>
  import myHeader from './header/Header'
  import banner from './banner/banner'
  import search from './search/search'
  import contentTitle from './title/title'

  export default {
    name: 'home',
    components: { myHeader, banner, search, contentTitle }
  }
</script>
<style lang="postcss">
  @component-namespace one{
    @b home{
      width: 1200px;
    }
  }
</style>
