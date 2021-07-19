<template>
  <div class="events">
    <div class="title">
      <h3 class="title__heading">Upcoming Events</h3>
    </div>

    <div class="slider">
      <Slick ref="slick" :options="slickOptions">
        <div v-for="slide in slides" :key="slide.id" class="slider__item">
          <a class="slider__link" :href="slide.url">
            <span>Coming Soon</span>
          </a>
        </div>
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
      slides: [
        { id: 1, url: '#' },
        { id: 2, url: '#' },
        { id: 3, url: '#' },
        { id: 4, url: '#' },
        { id: 5, url: '#' },
        { id: 6, url: '#' },
      ],
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

  @media screen and (max-width: 600px) {
    justify-content: center;
  }

  .title {
    width: 100%;
    text-align: left;
    margin: 0;
  }

  .title__heading {
    font-size: 1.8rem;
    margin: 0;

    @media screen and (max-width: 600px) {
      font-size: 1.4rem;
      text-align: center;
    }
  }

  .title__subheading {
    font-size: 1.1rem;
    color: #432e2d;
    opacity: 0.6;
    margin: 0.7rem 0;
  }

  .slider {
    @media screen and (max-width: 600px) {
      margin: 3.5rem 0;
    }
  }

  .slider__item {
    width: auto;
    height: 300px;
    background: #432e2d;
    border-right: 10px solid white;
  }

  .slider__link {
    display: grid;
    place-items: center;
    width: 100%;
    height: 100%;
    color: #fff;
    font-size: 1.5rem;
    text-decoration: none;
    text-transform: uppercase;
    box-shadow: inset 0 0 2000px 2000px #00000098;
  }

  .control {
    display: flex;
    align-items: center;
    @media screen and (max-width: 600px) {
      justify-content: center;
    }
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

    @media screen and (max-width: 600px) {
      height: 3rem;
      padding: 0 0.3rem;
    }

    &:hover {
      color: #fff;
      background: #432e2d;
      transform: scale(0.95);
    }
  }
}
</style>
