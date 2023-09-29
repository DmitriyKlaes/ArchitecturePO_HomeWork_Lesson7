<template>
  <section class="about">
    <div class="about__container">
      <article class="about__item">
        <h2 class="about__heading">18</h2>
        <p class="about__text">Месяцев учебы</p>
      </article>
      <img src="@/assets/img/line.png" alt="line" class="about__line" />
      <article class="about__item">
        <h2 class="about__heading">~250</h2>
        <p class="about__text">Выполненных домашних заданий</p>
      </article>
      <img src="@/assets/img/line.png" alt="line" class="about__line" />
      <article class="about__item">
        <h2 class="about__heading">100%</h2>
        <p class="about__text">из всех заданий на отлично</p>
      </article>
      <img src="@/assets/img/line.png" alt="line" class="about__line" />
      <article class="about__item">
        <h2 class="about__heading">0</h2>
        <p class="about__text">Предложений о работе</p>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Goals',
  data() {
    return {};
  },
  props: {},
  methods: {},
  computed: {},
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.about {
  height: 455px;
  padding-top: 150px;
  box-sizing: border-box;

  &__container {
    display: flex;
    max-width: 1080px;
    justify-content: space-between;
    align-items: center;
    height: 155px;
    margin: 0 auto;
  }

  &__item {
    text-align: center;
  }

  &__heading {
    @include fontStyle(85px, #646eca);
    letter-spacing: 1.7px;
  }

  &__text {
    font-family: $smallTextFont;
    @extend %secondaryTextstyle;
    letter-spacing: 0.22px;
  }
}
</style>
