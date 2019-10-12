<template>
  <Section class="intro" dots="true">
    <div class="container text-center">
      <div class="intro__message mb" hidden></div>

      <h1 class="intro__title">
        <span>Hey, I'm Cynthia 🙋</span>
         <Avatar class="intro__image"/>
        <transition name="rotate">
          <div
            class="intro__subtitle"
            v-if="currentText == 0"
            key="0"
          >A passionate software developer</div>
          <div
            class="intro__subtitle"
            v-else-if="currentText == 1"
            key="1"
          >The Vue Vixens Switzerland Chapter Leader</div>
          <div
            class="intro__subtitle"
            v-else-if="currentText == 2"
            key="2"
          >The Vue Berne Meetup Organizer</div>
        </transition>
      </h1>

      <!--<p class="intro__lead lead post mb">
        Feel free to follow me on
        <g-link href="https://twitter.com/lady_mashiro">Twitter</g-link>
      </p>-->
    </div>
  </Section>
</template>

<static-query>
query HomeIntro {
  metadata {
    gridsomeVersion
  }
}
</static-query>

<script>
import Avatar from "~/components/about/Avatar.vue";
export default {
  components: {
    Avatar
  },
  data() {
    return {
      currentText: 0
    };
  },
  mounted() {
    this._counter = setInterval(() => {
      this.currentText = (this.currentText + 1) % 3;
    }, 2500);
  },
  destroyed() {
    clearTimeout(this._counter);
  }
};
</script>

<style lang="scss">
.intro {
  padding: calc(2% + var(--space)) 0;

  &__title {
    font-size: 2rem;
    font-weight: 600;
    margin-left: auto;
    margin-right: auto;

    @media screen and (max-width: 850px) {
      & {
        font-size: 2rem;
      }
    }
  }

  &__subtitle {
    font-weight: 600;
    margin-left: auto;
    margin-right: auto;
    font-size: 1.5rem;
    @media screen and (max-width: 850px) {
      & {
        font-size: 1.5rem;
      }
    }
  }

  &__lead {
    max-width: 610px;
    margin-left: auto;
    margin-right: auto;
    font-size: 1.3rem;

    @media screen and (max-width: 850px) {
      & {
        font-size: 1rem;
      }
    }
  }

  &__info {
    font-size: 0.9rem;
  }

  &__image {
      margin-top: 30px;
  }
}
</style>
