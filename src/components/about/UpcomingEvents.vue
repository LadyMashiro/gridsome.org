<template>
  <Section class="upcoming-events">
    <div class="grid-cols grid-cols--gap-large grid-cols--full-md">
      <Card title="Upcoming Events">
        <h4>CMSs</h4>
        <p>Any Headless CMS, Contentful, WordPress, Drupal, Sanity.io, etc.</p>
        <h4>Data</h4>
        <p>Any APIs, Databases, AirTable, YAML, CSV, JSON, etc.</p>
        <h4>Markdown</h4>
        <p>Any Git-based CMS, Forestry, Netlify CMS, Blogs, Documentation.</p>

        <template slot="outer">
          <Dots class="hide-for-small" />
          <Dots class="dots--vertical show-for-small" />
        </template>
      </Card>

      <Card class="text-center flex-align-middle">
        <div class="works__logo">
          <vue-heart />
          <div class="works__pulse-bg"></div>
          <div class="works__pulse-bg"></div>
        </div>

        <p class="works__powered-by">
          Spread the
          <strong>Vue</strong> love 🙌
        </p>

        <template slot="outer">
          <Dots class="hide-for-small" />
          <Dots class="dots--vertical show-for-small" />
        </template>
      </Card>

      <Card title="Past Events">
        <ul class="title flex text-left flex--start">
          <li>
            Text
            <img src="/assets/static/src/assets/images/cynthia.png" class="title--image" width="28" height="28" />
          </li>
          <li class="title--date">(Nov 20th, 2019)</li>
        </ul>
        <p>Any Headless CMS, Contentful, WordPress, Drupal, Sanity.io, etc.</p>
        <h4>Data</h4>
        <p>Any APIs, Databases, AirTable, YAML, CSV, JSON, etc.</p>
        <h4>Markdown</h4>
        <p>Any Git-based CMS, Forestry, Netlify CMS, Blogs, Documentation.</p>
      </Card>
    </div>
  </Section>
</template>

<script>
import GraphQlLogo from "~/assets/images/graphql-logo.svg";
import VueLogo from "~/assets/images/vue-logo.svg";
import WebpackLogo from "~/assets/images/webpack-logo.svg";
import GridsomeLogo from "~/assets/images/gridsome-small-white.svg";
import Bullet from "~/assets/images/bullet.svg";
import Dots from "~/components/Dots.vue";
import IconTitle from "~/components/about/IconTitle.vue";
import VueHeart from "~/assets/images/vue-heart.svg";

export default {
  components: {
    Bullet,
    VueLogo,
    GridsomeLogo,
    WebpackLogo,
    GraphQlLogo,
    Dots,
    IconTitle,
    VueHeart
  }
};
</script>

<style lang="scss">
.works {
  .bullet-list li {
    margin-bottom: 0.3rem;
  }

  .card__inner {
    padding: 30px 40px;
  }

  @media screen and (max-width: 850px) {
    .card {
      margin-bottom: 40px;
    }
  }

  &__tools {
    font-weight: 500;
    border: 1px solid var(--border-color);
    max-width: 230px;
    border-radius: 4px;
    z-index: 9;
    margin: 0 auto !important;
    padding: 10px;

    li {
      margin-bottom: 0;
    }
  }

  &__logo {
    background-color: var(--bg);
    width: 100px;
    z-index: 1;
    position: relative;
    height: 100px;
    margin: 0 auto;
    margin-top: 18%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    border-radius: 100%;
    z-index: 0;
    margin-bottom: 1rem;
    animation: bounce 2s infinite;
    svg {
      width: 70px;
      height: 70px;
    }
  }

  &__pulse-bg {
    animation: pulse 2s infinite;
    border: 3px solid var(--primary-color);
    width: 90px;
    height: 90px;
    position: absolute;
    border-radius: 100%;
    opacity: 0.3;
    z-index: -1;

    + .works__pulse-bg {
      width: 75px;
      height: 75px;
      animation-delay: 0.2s;
    }
  }

  &__powered-by {
    opacity: 0.8;
    line-height: 1.3;
    padding-bottom: 1.2rem;
  }
}
</style>
