<template>
  <Section>
    <h2 class="text-center mb-x2">✨Upcoming Events</h2>
    <div class="grid-cols container grid-cols--gap-large grid-cols--full-md">
      <Card title="Oct 20th, 2019" class="sponsor text-center">
        <g-image src="~/assets/images/vue-bern.png" alt="Vue Berne" />
        <h3>Vue Berne Meetup</h3>
        <p>
          I just recently created the
          <a
            href="https://www.meetup.com/Vue-Bern/"
            rel="noopener"
            target="_blank"
          >Vue Berne Meetup</a> since there were a lot of people requesting it and I had this plan in my mind already for quite some time.
        </p>
        <p>
          We will have the amazing
          <a
            href="https://twitter.com/gustojs?s=17"
            rel="noopener"
            target="_blank"
          >Gusto</a> here who will have a talk & be up for some discussons/panels.
        </p>
        <template slot="outer">
          <Dots class="hide-for-small" />
          <Dots class="dots--vertical show-for-small" />
        </template>
      </Card>
      <Card title="Nov 14th, 2019" class="sponsor text-center">
        <g-image src="~/assets/images/vue-basel.png" alt="Vue Berne" />
        <h3>Vue Basel Meetup</h3>
        <p>
          <a href="https://www.meetup.com/Vue-Basel/" rel="noopener" target="_blank">Vue Basel</a> is a great meetup for people who are working with (or just interested in) the Vue.js framework where you have the chance to talk about experiences and show off cool projects.
        </p>
        <p>
          It's a regularly scheduled meetup organized by the amazing
          <a href="https://twitter.com/gustojs?s=17" rel="noopener" target="_blank">Max Gfeller</a> 🙌, Lead Frontend Developer at <a href="https://www.cyon.ch/" rel="noopener" target="_blank">cyon</a>.
        </p>
        <template slot="outer">
          <Dots class="hide-for-small" />
          <Dots class="dots--vertical show-for-small" />
        </template>
      </Card>
      <Card title="Nov 25th, 2019" class="sponsor text-center">
        <g-image src="~/assets/images/vuevixens-logo.png" alt="Vue Berne" />
        <h3>Vue Vixens 🇵🇱 full-day workshop</h3>
        <p>
          I will be co-organizing the workshop for
          <a
            href="https://www.meetup.com/Vue-Bern/"
            rel="noopener"
            target="_blank"
          >Frontend-con.io</a>, which will be the first Vue Vixens Workshop in Poland.
        </p>
        <template slot="outer">
          <Dots class="hide-for-small" />
          <Dots class="dots--vertical show-for-small" />
        </template>
      </Card>
      <Card title="Nov 26th - 27th, 2019" class="sponsor text-center">
        <g-image src="~/assets/images/frontend-con.png" alt="Vue Berne" style="background-color: var(--body-color); padding: 6px; border-radius:3px;"/>
        <h3>Frontend-con.io</h3>
        <p>
          I am very excited to be able to join the
          <a
            href="https://www.meetup.com/Vue-Bern/"
            rel="noopener"
            target="_blank"
          >Frontend-con.io</a> in Warsaw. It will surely be an amazing experience.
        </p>
      </Card>
    </div>
  </Section>
</template>

<script>
import Dots from "~/components/Dots.vue";
export default {
  components: {
    Dots
  }
};
</script>

<style lang="scss">
.sponsor {
  img {
    max-height: 55px;
    width: auto;
  }
}
</style>
