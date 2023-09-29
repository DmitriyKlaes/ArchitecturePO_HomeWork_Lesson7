<template>
  <div>
    <header class="header">
      <div class="header__name">KEEP YOUR DREAMS</div>
      <div class="header__nav">
        <router-link to="/" class="header__link">Home</router-link>
        <router-link to="/about" class="header__link">About</router-link>
        <router-link to="/goals" class="header__link">Goals</router-link>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 50px;
  max-width: $siteWidth;
  margin: 0 auto;

  &__name {
    display: flex;
    align-items: center;
    gap: 10px;
    @include fontStyle(40px, $textColor);
  }

  &__nav {
    display: flex;
    justify-content: space-between;
    width: 240px;
  }

  &__link {
    font-family: $smallTextFont;
    text-align: center;
    @include fontStyle(20px, $textColor);
  }
}
</style>
