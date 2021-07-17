<template>
  <div>
    <Hero />
    <Events />
  </div>
</template>

<script>
import Hero from '@/components/landing/Hero.vue'
import Events from '@/components/landing/Events.vue'

export default {
  components: {
    Hero,
    Events,
  },
}
</script>
