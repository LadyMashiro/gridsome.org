<template>
  <ul class="title flex text-left flex--start">
    <li>
      {{ title }} <title-image class="title--image" width="28" height="28" alt="Vue" />
    </li>
    <li class="title--date" v-if="date.length > 0">(Nov 20th, 2019)</li>
  </ul>
</template>

<script>
import titleImage from '~/assets/images/vue-heart.svg'
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: false,
      default: ''
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
    max-width: 400px;
    border-radius: 4px;
    z-index: 9;
    margin: 0 auto!important;
    padding: 6px;
    font-weight: 700;
    // font-size: 1.5rem;
    // background-color: var(--dark-bg);

    &--date {
        color: var(--primary-color-dark);
        font-size: 90%;
    }

    &--image {
      margin: -3px 3px;
    }

    li {
        margin: 0 2px;
    }
}
</style>