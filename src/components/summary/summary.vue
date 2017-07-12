<template>
  <div >
    <horizontal v-if="direction === 'h'" :overlap="overlap" :size="size" :summaryData="summaryData"></horizontal>
  </div>
</template>
<script>
  import Horizontal from './Horizontal'
  export default{
    name: 'my-summary',
    components: { Horizontal },
    props: {
      summaryData: Array,
      direction: String,
      size: String,
      overlap: Boolean
    }
  }
</script>
