<template>
  <ul class="title flex text-center flex--space-between">
    <li>
      <title-image width="28" height="28" alt="Vue" /> Vue.js
    </li>
    <li class="title--date">(Nov 20th, 2019)</li>
  </ul>
</template>

<script>
import titleImage from '~/assets/images/vue-logo.svg'
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    }
  },
  components: {
      titleImage
  }
};
</script>

<style lang="scss">
  .title {
    font-weight: 500;
    // border: 1px solid var(--border-color);
    max-width: 230px;
    border-radius: 4px;
    z-index: 9;
    margin: 0 auto!important;
    padding: 6px;
    // background-color: var(--dark-bg);

    &--date {
        color: var(--primary-color-dark);
        font-size: 90%;
    }

    li {
        margin: 0 2px;
    }
}
</style>