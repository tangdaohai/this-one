<template>
  <div class="one-title">
    <div class="one-title__type">{{title}}</div>
    <div class="one-title__list">
      <span class="type" v-for="type in types" :key="type">{{type}}</span>
    </div>
  </div>
</template>
<script>
  import './title.css'
  export default{
    name: 'content-title',
    props: {
      title: String,
      types: Array
    }
  }
</script>
