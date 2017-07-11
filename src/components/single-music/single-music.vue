<template>
  <div class="one-single">
    <div class="one-single__img">
      <img src="../../assets/m_58579a7a3b2a8.jpg" alt="">
    </div>
    <div class="one-single__description">
      <div class="one-single__title">
        <i class="arrow"></i>
        <span>我们终将奔赴向前</span>
        <img src="../../assets/play_button.png" alt="">
      </div>
      <div class="one-single__conent">
        <span>当和熙春风吹拂过细节与平淡的山顶，当往昔的时光洒向林间的湖泊，这温暖如同爱人的怀抱，美好且沉默。我们手握着夜间孤芳自赏的花朵，在流离失所的纯白和微妙的存粹中，用一种自信满满的暖手的暖色调涂抹着世界。</span>
        <span>我们终将奔赴向前</span>
      </div>
      <div class="one-single__like">
        <span class="pubtime">2017.03.23</span>
        <like :likeCount="122"></like>
      </div>
    </div>
  </div>
</template>
<script>
  import like from '../like/like'
  import './single-music.css'
  export default{
    name: 'single-music',
    components: { like }
  }
</script>
