<template>
  <main>
    <section class="promo">
      <article class="promo__info">
        <h1 class="promo__head">Это обычная главная страница</h1>
        <div class="promo__buttons">
          <MainButton linkName="Обо мне" linkUrl="/about" />
          <MainButton linkName="Цели" linkUrl="/goals" />
        </div>
      </article>
    </section>
  </main>
</template>

<script>
import MainButton from '@/components/MainButton.vue';

export default {
  name: 'Home',
  data() {
    return {};
  },
  methods: {},
  components: { MainButton },
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.promo {
  background-image: url('@/assets/img/home-img.jpg');
  background-repeat: no-repeat;
  background-size: contain;
  height: 900px;
  border-radius: 70px;
  max-width: $siteWidth;
  margin: 0 auto;

  &__buttons {
    display: flex;
    width: 80%;
    justify-content: space-between;
  }

  &__info {
    margin-top: 50px;
    padding-top: 10px;
    padding-bottom: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 90%;
    align-items: center;
  }

  &__head {
    @include fontStyle(65px, $textColor);
    margin-bottom: 18px;
  }
}
</style>
