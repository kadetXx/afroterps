<template>
  <div class="join">
    <h1 class="title">Join Afroterps Community</h1>

    <p class="content">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>

    <div class="cta">
      <a class="cta__link" href="#">
        <button class="cta__button">
          Proceed To Telegram
          <i class="fab fa-telegram-plane"></i>
        </button>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Join',
}
</script>

<style lang="scss">
.join {
  min-height: 100vh;
  padding: 4rem 5%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;
  text-align: center;

  @media screen and (max-width: 600px) {
    align-items: flex-start;
    text-align: left;
  }
}

.title {
  margin-bottom: 1rem;
  font-size: 1.8rem;

  @media screen and (max-width: 700px) {
    font-size: 1.3rem;
  }
}

.content {
  padding: 0 12%;
  font-size: 1.1rem;
  opacity: 0.7;
  line-height: 2;

  @media screen and (max-width: 700px) {
    padding: 0 0;
    font-size: 1rem;
  }
}

.cta {
  margin-top: 2rem;
  width: 100%;
}

.cta__link {
  width: 100%;
  text-decoration: none;
}

.cta__button {
  width: 40%;
  padding: 1rem;
  border-radius: 30px;
  border: none;
  background: #3bb3df;
  color: #fff;
  font-weight: 600;
  font-size: 1.1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: auto;

  @media screen and (max-width: 700px) {
    width: 100%;
  }

  i {
    margin-left: 1rem;
  }
}
</style>
