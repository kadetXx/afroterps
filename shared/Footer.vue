<template>
  <footer>
    <span>Copyright {{ date }} Afroterps</span>
  </footer>
</template>

<script>
export default {
  name: 'footer',
  data() {
    return {
      date: (new Date()).getFullYear()
    }
  }
}
</script>

<style lang="scss" scoped>
footer {
  display: grid;
  place-items: center;
  background: #442f2e;
  color: #ffff;
  padding: 0.5rem 5%;
  margin-top: auto;
}
</style>