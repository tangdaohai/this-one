<template>
  <div class="one-home">
    <my-header></my-header>
  </div>
</template>
<script>
  import myHeader from './header/Header'
  export default {
    name: 'home',
    components: { myHeader }
  }
</script>
<style lang="postcss">
  @component-namespace one{
    @b home{
      width: 1200px;
    }
  }
</style>
