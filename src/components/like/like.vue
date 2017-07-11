<template>
  <div class="one-like">
    <img class="one-like__icon" src="../../assets/unlike.png" alt="like">
    <span>({{likeCount || 0}})</span>
  </div>
</template>
<script>
  export default{
    name: 'like',
    props: {
      likeCount: Number
    }
  }
</script>
<style lang="postcss">
  @component-namespace one{
    @b like{
      font-size: 13px;
      letter-spacing: 2px;
      color: #999;
      margin-right: 20px;

      @e icon{
        vertical-align: bottom;
        margin-right: 6px;
      }
    }
  }
</style>
