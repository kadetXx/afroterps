<template>
  <div ref="hero" class="hero">
    <div class="hero__heading">
      Africa's <b>Online</b> Platform for <b>professional</b>
      <b>Conference</b> Interpreters.
    </div>
    <button class="hero__button" @click="scroll">
      <span class="material-icons hero__button-icon"> south </span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  methods: {
    scroll() {
      document.querySelector('.events').scrollIntoView({
        behavior: 'smooth',
        block: 'center',
      })
    },
  },
}
</script>

<style lang="scss" scoped>
.hero {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  text-align: center;
  padding: 0 10%;
  background: url('@/assets/images/afroterps-bg.png');
  background-position: center;
  background-size: cover;
  box-shadow: inset 0 0 2000px 2000px #000000e3;

  &__heading {
    font-size: 3rem;
    color: #fff;
    font-weight: 400;
    padding: 0 5%;

    @media screen and (max-width: 800px) {
      font-size: 1.8rem;
    }

    @media screen and (max-width: 600px) {
      padding: 0 0%;

      font-size: 1.5rem;
    }

    b {
      font-weight: 600;
    }
  }

  &__button {
    background: transparent;
    padding: 1.5rem 0.7rem;
    border: 1px solid #442f2e;
    border-radius: 30px;
    color: #ffd792;
    position: absolute;
    bottom: 2rem;
    cursor: pointer;
    outline: none;

    @media screen and (max-width: 600px) {
      padding: 1.2rem 0.7rem;
    }
  }

  &__button-icon {
    animation-name: bounce;
    animation-duration: 0.7s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;

    @media screen and (max-width: 600px) {
      font-size: 1.2rem;
    }
  }

  @keyframes bounce {
    0% {
      transform: translateY(0);
    }

    25% {
      transform: translateY(-5px);
    }

    50% {
      transform: translateY(0);
    }

    75% {
      transform: translateY(5px);
    }

    100% {
      transform: translateY(0);
    }
  }
}
</style>
