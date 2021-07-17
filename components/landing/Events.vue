<template>
  <div class="events">
    <div class="title">
      <h3 class="title__heading">Upcoming Events</h3>
    </div>

    <div class="slider">
      <Slick :options="slickOptions" ref="slick">
        <div class="slider__item"><a href="#"> </a></div>
        <div class="slider__item"><a href="#"> </a></div>
        <div class="slider__item"><a href="#"> </a></div>
        <div class="slider__item"><a href="#"> </a></div>
        <div class="slider__item"><a href="#"> </a></div>
        <div class="slider__item"><a href="#"> </a></div>
      </Slick>
    </div>

    <div class="control">
      <button class="control__button" @click="prev">
        <span class="material-icons"> chevron_left </span>
      </button>
      <button class="control__button" @click="next">
        <span class="material-icons"> chevron_right </span>
      </button>
    </div>
  </div>
</template>

<script>
import Slick from 'vue-slick'
import 'slick-carousel/slick/slick.css'

export default {
  name: 'Events',
  components: {
    Slick,
  },
  data() {
    return {
      slickOptions: {
        dots: false,
        arrows: false,
        infinite: false,
        speed: 300,
        slidesToShow: 3,
        slidesToScroll: 1,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 3,
            },
          },
          {
            breakpoint: 600,
            settings: {
              slidesToShow: 2,
            },
          },
          {
            breakpoint: 480,
            settings: {
              slidesToShow: 1,
            },
          },
        ],
      },
    }
  },
  methods: {
    next() {
      this.$refs.slick.next()
    },

    prev() {
      this.$refs.slick.prev()
    },
  },
}
</script>

<style lang="scss" scoped>
.events {
  height: 100vh;
  padding: 4rem 5%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  .title {
    width: 100%;
    text-align: left;
  }

  .title__heading {
    font-size: 2rem;
    margin-block: 0;
  }

  .title__subheading {
    font-size: 1.1rem;
    color: #432e2d;
    opacity: 0.6;
    margin: 0.7rem 0;
  }

  .slider {
    margin-top: 3rem;
  }

  .slider__item {
    width: auto;
    height: 300px;
    background: #432e2d;
    border-right: 10px solid white;
  }

  .control {
    display: flex;
    align-items: center;
    margin-top: 3rem;
  }

  .control__button {
    background: transparent;
    border: 2px solid #432e2d;
    color: #432e2d;
    height: 3rem;
    padding: 0 0.5rem;
    display: grid;
    place-items: center;
    margin-right: 1rem;
    transition: all 0.2s linear;

    &:hover {
      color: #fff;
      background: #432e2d;
      transform: scale(0.95);
    }
  }
}
</style>
