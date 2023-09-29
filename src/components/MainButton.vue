<template>
  <div>
    <router-link :to="linkUrl" class="link">
      <div class="button">
        {{ linkName }}
        <svg
          width="19"
          height="17"
          viewBox="0 0 19 17"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M2 8.43542L15.7232 8.29857M10.6182 1.91138L17.1412 8.43436L10.4868 15.0887"
            stroke="#CDA274"
            stroke-width="2"
            stroke-linecap="square"
            stroke-linejoin="round"
          />
        </svg>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'MainButton',
  created() {},
  data() {
    return {};
  },
  props: {
    linkName: String,
    linkUrl: String,
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_mixins.scss';
@import '@/assets/styles/_vars.scss';
@import '@/assets/styles/styles.scss';

.link {
  display: block;
  border-radius: 18px;
  margin-top: 21px;
  max-width: 220px;
  height: 75px;
  overflow: hidden;
  box-shadow: 0px 10px 20px 0px rgba(192, 192, 192, 0.35);
  background: $textColor;
}

.button {
  height: 100%;
  gap: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  @include fontStyle(18px, #fff);
  font-family: $smallTextFont;
  letter-spacing: 0.36px;
  min-width: 200px;
}
</style>
