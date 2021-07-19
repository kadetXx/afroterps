<template>
  <div>
    <Hero />
    <Events />
    <Newsletter />
  </div>
</template>

<script>
import Hero from '@/components/landing/Hero.vue'
import Events from '@/components/landing/Events.vue'
import Newsletter from '@/components/landing/Newsletter.vue'

export default {
  components: {
    Hero,
    Events,
    Newsletter
  },
}
</script>
