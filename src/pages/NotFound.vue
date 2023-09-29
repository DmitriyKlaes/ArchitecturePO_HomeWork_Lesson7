<template>
  <main class="main">
    <article class="info">
      <h1 class="head">404</h1>
      <p class="text">We are sorry, but the page you requested was not found</p>
      <MainButton linkName="На главную" linkUrl="/" />
    </article>
  </main>
</template>

<script>
import MainButton from '@/components/MainButton.vue';

export default {
  name: 'NotFound',
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
  components: { MainButton },
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.main {
  max-height: 1040px;
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 1560px;
  margin: 50px auto 100px;
  gap: 20px;
}
.info {
  max-width: 570px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.head {
  @include fontStyle(250px, #cda274);
}
.text {
  color: $textColor;
  font-size: 35px;
  font-style: normal;
  font-weight: 400;
  line-height: 150%;
  letter-spacing: 0.35px;
  text-align: center;
}
</style>
