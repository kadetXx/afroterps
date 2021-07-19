<template>
  <div ref="newsletter" class="newsletter">
    <div class="title">
      <h3 class="title__heading">Subscribe To Our Newsletter</h3>
      <p class="title__subheading">
        Be the first to be informed about our events, seminars, offers, tips and
        promotions for free. We promise not to spam your email and you can
        unsubscribe at anytime.
      </p>
    </div>

    <form class="form">
      <input
        class="form__input"
        type="email"
        name="email"
        placeholder="Your email address"
      />
      <button class="form__button" type="submit">Subscribe</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Newsletter',
}
</script>

<style lang="scss" scoped>
.newsletter {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background: #efefef;
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

.form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 40%;

  @media screen and (max-width: 800px) {
    width: 100%;
  }
}

.form__input {
  width: 100%;
  border: 1px solid #916b367c;
  padding: 0.9rem;
  outline: none;
  border-radius: 30px;
  text-align: center;
  color: #432e2dd3;

  &::placeholder {
    font-size: 1rem;
    color: #916b36a2;
  }
}

.form__button {
  width: 100%;
  outline: none;
  padding: 0.9rem;
  background: #52b75f;
  border: none;
  color: #fff;
  margin-top: 0.5rem;
  border-radius: 30px;
  font-weight: 600;
  font-size: 1rem;
}
</style>
