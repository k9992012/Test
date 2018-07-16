<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl"/>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: "HomeSwiper",
    data() {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination'
          },
          loop: true
        },
        swiperList: [{
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/de/df09fa61aed2d502.jpg_750x200_67472739.jpg'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff

  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.667%
    background: #eee
    .swiper-img
      width: 100%
</style>