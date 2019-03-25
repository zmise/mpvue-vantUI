<template>
  <div class="container">
    <swiper
      class="swiper"
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
      circular
    >
      <block v-for="(item, index) in imgUrls" :index="index" :key="key">
        <swiper-item>
          <image :src="item" class="slide-image" mode="aspectFill " width="355" height="150"/>
        </swiper-item>
      </block>
    </swiper>

    <button @tap="changeIndicatorDots">indicator-dots</button>
    <button @tap="changeAutoplay">autoplay</button>
    <slider @change="intervalChange" show-value min="500" max="2000"/>
    <slider @change="durationChange" show-value min="1000" max="10000"/>
    <swiper
      class="swiper"
      autoplay
      indicator-color="#a39f99"
      indicator-active-color="#f49641"
      indicator-dots
      interval="2000"
      duration="1000"
      previous-margin="30px"
      next-margin="30px"
      circular
      @change="bindchange"
      :style="{height: swiperHeight + 'px'}"
    >
      <block v-for="(item, index) in imgUrls" :index="index" :key="key">
        <swiper-item>
          <image
            :src="item"
            :class="swiperIndex == index ?'active slide-image':'quiet slide-image'"
            mode="aspectFill "
            width="355"
            height="150"
          />
        </swiper-item>
      </block>
    </swiper>
  </div>
</template>
<script>
export default {
  data () {
    return {
      imgUrls: [
        'https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640',
        'https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640',
        'https://images.unsplash.com/photo-1551446591-142875a901a1?w=640'
      ],
      indicatorDots: false,
      autoplay: true,
      interval: 2000,
      duration: 1000,
      swiperIndex: 0
    }
  },
  methods: {
    changeIndicatorDots (e) {
      this.indicatorDots = !this.indicatorDots
    },
    changeAutoplay (e) {
      this.autoplay = !this.autoplay
    },
    intervalChange (e) {
      console
      this.interval = e.detail.value
    },
    durationChange (e) {
      this.duration = e.detail.value
    },

    bindchange (e) {
      this.swiperIndex = e.mp.detail.current
    }
  }
}
</script>
<style lang="less" scoped>
.swiperClass {
  margin: 0;
  margin-top: 10px;
}

.slide-image {
  width: 100%;
  height: 90%;
  border-radius: 10px;
  position: relative;
}

image.active {
  transform: none;
  transition: all 0.2s ease-in 0s;
}

image.quiet {
  transform: scale(0.8333333);
  transition: all 0.2s ease-in 0s;
}
</style>
