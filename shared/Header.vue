<template>
  <header :class="overlay ? 'overlay' : ''">
    <NuxtLink to="/" class="logo">
      <img class="logo__image" src="~assets/svgs/logo.svg" alt="afroterps" />
    </NuxtLink>

    <nav :class="expanded ? 'nav nav--expanded' : 'nav'">
      <ul class="nav__menu">
        <li class="nav__item">
          <NuxtLink to="/" class="nav__link"> Home </NuxtLink>
        </li>

        <li class="nav__item">
          <NuxtLink to="/community" class="nav__link">
            Join Community
          </NuxtLink>
        </li>

        <li class="nav__item">
          <NuxtLink to="/contact" class="nav__link"> Contact Us </NuxtLink>
        </li>
      </ul>
    </nav>

    <button
      :class="expanded ? 'hamburger hamburger--expanded' : 'hamburger'"
      @click="toggleMenu()"
    >
      <span class="hamburger__bar hamburger__bar--one"></span>
      <span class="hamburger__bar hamburger__bar--two"></span>
      <span class="hamburger__bar hamburger__bar--three"></span>
    </button>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      expanded: false,
    }
  },

  computed: {
    overlay() {
      return this.$route.name === 'index'
    },
  },

  watch: {
    expanded() {
      if (this.expanded) {
        document.body.style.overflow = 'hidden'
      } else {
        document.body.style.overflow = 'auto'
      }
    },
  },

  methods: {
    toggleMenu: function name() {
      this.expanded = !this.expanded
    },
  },
}
</script>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 5%;
  z-index: 8;
  box-shadow: 0 2px 12px 0 rgb(36 50 66 / 8%);
  overflow: hidden;

  .logo {
    font-size: 1.5rem;
    color: #442f2e;
    text-decoration: none;
    z-index: 10;
    display: flex;
    align-items: center;
  }

  .logo__image {
    width: 120px;
    height: auto;

    @media screen and (max-width: 600px) {
      width: 90px;
    }
  }

  .nav__menu {
    display: flex;
    align-items: center;
    list-style: none;
    padding: 0;

    @media screen and (max-width: 600px) {
      width: 100%;
      height: 100%;
      flex-direction: column;
      justify-content: center;
    }
  }

  .nav__item {
    margin-left: 2rem;

    @media screen and (max-width: 600px) {
      margin: 0 0 2rem;
      transform: translateY(200vh);
    }
  }

  .nav__link {
    text-decoration: none;
    color: #442f2e;

    &:hover {
      color: #8f713e;
    }
  }

  .hamburger {
    display: none;
    background: transparent;
    border: none;
    z-index: 10;
    position: relative;

    @media screen and (max-width: 600px) {
      display: grid;
      place-items: center;
    }

    &__bar {
      width: 1.7rem;
      height: 2px;
      background: #c08f3d;
      margin: 0.12rem 0;

      &--two {
        margin-left: 0.3rem;
        width: 1.4rem;
        transition: all ease-in 0.3s;
      }

      &--three {
        margin-left: 0.3rem;
        width: 1.4rem;
      }
    }

    &--expanded {
      min-height: 12px;

      .hamburger__bar {
        margin: 0;
        width: 1.4rem;
      }

      .hamburger__bar--one {
        position: absolute;
        transform: rotate(45deg);
      }

      .hamburger__bar--two {
        margin-left: 0;
        transform: translateX(50vw);
      }

      .hamburger__bar--three {
        margin-left: 0;
        position: absolute;
        transform: rotate(-45deg);
      }
    }
  }

  .nav {
    @media screen and (max-width: 600px) {
      position: fixed;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      opacity: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      transform: translateY(-100vh);
    }
  }

  .nav--expanded {
    transition: all linear 0.3s;

    @media screen and (max-width: 600px) {
      z-index: 5;
      opacity: 1;
      background: #ffffff;
      transform: translateY(0);
    }

    .nav__item {
      transition: all linear 0.4s;
      transform: translateY(0);
    }
  }
}

.overlay {
  padding-top: 2rem;
  padding-bottom: 2rem;
  box-shadow: none;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;

  .logo,
  .nav__link {
    color: #c08f3d;

    &:hover {
      color: #8f713e;
    }
  }
}
</style>
