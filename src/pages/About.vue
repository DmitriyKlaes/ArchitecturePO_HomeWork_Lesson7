<template>
  <main class="main">
    <h1 class="head">Тут некоторая информация обо мне и фотки</h1>
    <swiper
      :style="{
        '--swiper-navigation-color': '#000',
        '--swiper-pagination-color': '#000',
      }"
      :zoom="true"
      :navigation="true"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide v-for="img in prodjectDetailsSwiperImgs" :key="img.id">
        <div class="swiper-zoom-container">
          <img class="swiper-img" :src="img" />
        </div>
      </swiper-slide>
    </swiper>
  </main>
</template>

<script>
import { mapState } from 'vuex';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Zoom, Navigation, Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/zoom';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import MainButton from '@/components/MainButton.vue';

export default {
  name: 'About',
  setup() {
    return {
      modules: [Zoom, Navigation, Pagination],
    };
  },
  components: {
    MainButton,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {};
  },
  methods: {},
  computed: {
    ...mapState(['prodjectDetailsSwiperImgs']),
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.main {
  margin: 0 auto;
  width: $siteWidth;
}

.head {
  @include fontStyle(30px, green);
  text-align: center;
  padding-top: 50px;
}
.swiper {
  width: 100%;
  height: 870px;
  max-width: $siteWidth;
  margin-bottom: 100px;
  border-radius: 70px;
}

.swiper-slide {
  overflow: hidden;
}

.swiper-img {
  width: 80%;
  height: 80%;
}
</style>
