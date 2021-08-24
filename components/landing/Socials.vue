<template>
  <div ref="socials" class="socials">
    <div class="title">
      <h3 class="title__heading">Follow Our Socials</h3>
      <p class="title__subheading">
        Stay on track with the lastest by following our social handles
      </p>
    </div>

    <div class="socials__icons">
      <a href="https://web.facebook.com/groups/353264166281462" target="_blank">
        <i class="fab fa-facebook-f"></i>
      </a>
      <a href="https://twitter.com/afroterps" target="_blank">
        <i class="fab fa-twitter"></i>
      </a>
      <a href="https://www.youtube.com/channel/UCp_-SIgiMYb1YDWhT0TH-tw/featured" target="_blank">
        <i class="fab fa-youtube"></i>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Socials',
}
</script>

<style lang="scss" scoped>
.socials {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background: #efefef;
  background: linear-gradient(
    0deg,
    rgba(239, 239, 239, 1) 66%,
    rgba(255, 255, 255, 1) 100%
  );
  padding: 4rem 5%;
}

.title {
  margin-bottom: 2rem;
  text-align: center;
  width: 50%;

  @media screen and (max-width: 700px) {
    width: 100%;
  }
}

.title__heading {
  font-size: 2rem;
  margin-top: 0;
  margin-block: 1rem;

  @media screen and (max-width: 600px) {
    font-size: 1.5rem;
  }
}

.title__subheading {
  margin: 0;
  opacity: 0.6;
  font-size: 1.05rem;

  @media screen and (max-width: 600px) {
    font-size: 1rem;
  }
}

.socials {
  &__icons {
    display: flex;
    justify-content: center;

    a {
      font-size: 4rem;
      margin: 0 1rem;
      color: #442f2e;
      transition: all 0.3s;

      @media screen and (max-width: 600px) {
        font-size: 2.5rem;
      }

      &:hover {
        transform: scale(1.1);
      }
    }
  }
}
</style>
