<template>
  <div class="hero">
    <div class="hero__heading">
      Africa's <b>Online</b> Platform for <b>professional</b> <b>Conference</b> Interpretations <b>services</b> and training.
    </div>
    <!-- <div class="hero__socials">
      <a href="/" class="hero__icon">
        <i class="fab fa-facebook-f"></i>
      </a>
      <a href="/" class="hero__icon">
        <i class="fab fa-youtube"></i>
      </a>
      <a href="/" class="hero__icon">
        <i class="fab fa-whatsapp"></i>
      </a>
      <a href="/" class="hero__icon">
        <i class="fab fa-twitter"></i>
      </a>
    </div> -->

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
      window.scrollY = window.innerHeight
    }
  }
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
  background: url('@/assets/images/conference-one.jpg');
  background-position: center;
  background-size: cover;
  box-shadow: inset 0 0 2000px 2000px #000000e3;

  &__heading {
    font-size: 3rem;
    color: #fff;
    font-weight: 400;
    padding: 0 5%;

    b {
      font-weight: 600;
    }
  }

  &__socials {
    margin-top: 1rem;
  }

  &__icon {
    font-size: 2rem;
    margin: 0 0.4rem;
    color: #ffd792;

    &:hover {
      color: #442f2e;
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
  }

  &__button-icon {
    animation-name: bounce;
    animation-duration: 0.7s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
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
