<template>
  <Layout class="layout-homepage">

    <LazyHydrate when-idle>
      <intro-cynthia />
    </LazyHydrate>

    <!--<IconTitle title="Upcoming Events" image="sparkles.png"/>-->

    <!--<LazyHydrate when-visible>
      <upcoming-events />
    </LazyHydrate>-->

    <LazyHydrate when-visible>
      <event-cards />
    </LazyHydrate>

    <LazyHydrate when-visible>
      <home-examples />
    </LazyHydrate>
    
  </Layout>
</template>

<script>
import LazyHydrate from 'vue-lazy-hydration'
import HomeIntroSimple from '@/components/home/HomeIntroSimple.vue'
import HomeHowItWorkSimple from '@/components/home/HomeHowItWorkSimple.vue'
import HomeBlog from '@/components/home/HomeBlog.vue'
import HomeFeatures from '@/components/home/HomeFeatures.vue'
import HomeExamples from '@/components/home/HomeExamples.vue'
import HomeCommunity from '@/components/home/HomeCommunity.vue'
import HomeConnect from '@/components/home/HomeConnect.vue'

import UpcomingEvents from '@/components/about/UpcomingEvents.vue'
import IconTitle from '@/components/about/IconTitle.vue'
import IntroCynthia from '@/components/about/IntroCynthia.vue'
import EventCards from '@/components/about/EventCards.vue'

export default {
  components: {
    LazyHydrate,
    HomeIntroSimple,
    HomeHowItWorkSimple,
    HomeExamples,
    HomeCommunity,
    HomeConnect,
    HomeFeatures,
    HomeBlog,
    UpcomingEvents,
    IconTitle,
    IntroCynthia,
    EventCards
  },
  
  metaInfo: {
    title: 'Modern Site Generator for Vue.js'
  }
}
</script>

<style>
@media screen and (min-width: 850px) {
  .layout-homepage header{
    border-color: transparent;  
  }
}
</style>


