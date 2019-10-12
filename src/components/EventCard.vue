<template>
  <div class="event-card" :class="{'event-card--has-link' : link}">
    <g-link v-if="link" class="event-card__link" :to="link">Read more</g-link>
    <div class="event-card__imageTop" v-if="$slots.imageTop">
      <slot name="imageTop"></slot>
    </div>
    <div class="event-card__title" v-if="title">
      <span>
        <ul class="title flex text-center flex--space-between">
          <li>
            <title-image width="28" height="28" alt="Vue" />
            {{ title }}
          </li>
          <li class="title--date">(Nov 20th, 2019)</li>
        </ul>
      </span>
    </div>
    <div v-if="image" class="event-card__image">
      <g-image :src="image" />
    </div>
    <div class="event-card__inner">
      <slot />
    </div>
    <slot name="outer" />
  </div>
</template>

<script>
export default {
  props: ["link", "image", "title"],
  computed: {
    cardClasses() {
      let classes = [];
      if (this.gradient) classes.push("gradient-" + this.gradient);
      return classes;
    }
  }
};
</script>

<style lang="scss">
.event-card {
  border: 1px solid var(--border-color-darker);
  border-radius: 4px;
  background-color: var(--bg);
  transition: color.3s, box-shadow 0.3s, transform 0.3s;
  position: relative;
  z-index: 1;

  &__title {
    text-align: center;
    width: 100%;
    margin-top: -16px;

    span {
      display: inline-block;
      padding: 2px 12px 4px;
      background-color: var(--dark-bg);
      color: #fff;
      border-radius: 3px;
      font-weight: 500;
      font-size: 1rem;
      letter-spacing: 0.5px;
    }
  }

  &__image {
    border-radius: 4px 4px 0 0;
    overflow: hidden;
    border-bottom: 1px solid var(--border-color);
    img {
      margin: 0;
      width: 100%;
    }
  }

  &__inner {
    padding: var(--space);
    overflow: hidden;
    position: relative;
  }

  &[class*="container"] &__inner {
    padding-left: 0;
    padding-right: 0;
  }

  .section--dark & {
    background-color: var(--dark-bg);
    border-color: rgba(255, 255, 255, 0.1);
  }

  &__link {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    overflow: hidden;
    text-indent: -9999px;
    z-index: 1;

    &:focus {
      opacity: 1;
      outline: 2px auto -webkit-focus-ring-color;
    }
  }

  a:not(.event-card__link) {
    position: relative;
    z-index: 1;
  }

  &--has-link:hover {
    transform: translateY(-3px);
    box-shadow: var(--glow);
    color: currentColor;
  }

  h2,
  h3,
  h4 {
    margin-bottom: 0.5rem;
  }

  p:not(:last-child) {
    margin-bottom: 1.2rem;
  }
}
</style>
