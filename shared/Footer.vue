<template>
  <footer>
    <span>&#169; Copyright {{ date }}, Afroterps</span>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      date: new Date().getFullYear(),
    }
  },
}
</script>

<style lang="scss" scoped>
footer {
  display: grid;
  place-items: center;
  background: #442f2e;
  color: #ffff;
  padding: 1rem 5%;
  margin-top: auto;

  span {
    opacity: 0.7;
  }
}
</style>
