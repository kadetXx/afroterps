<template>
  <div>
    <Hero />
    <Events />
    <Socials />
  </div>
</template>

<script>
import Hero from '@/components/landing/Hero.vue'
import Events from '@/components/landing/Events.vue'
import Socials from '~/components/landing/Socials.vue'

export default {
  components: {
    Hero,
    Events,
    Socials
  },
}
</script>
