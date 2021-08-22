<template>
  <div class="join">
    <h1 class="title">Join The Afroterps Community</h1>

    <p class="content">
      Afroterps is a platform for promoting the profession of conference
      interpreting in africa. We do this by bringing together profrssional
      conference interpreters of all ages from all over the continent to discuss
      issues relating to conference interpreting.
    </p>

    <p class="content">
      Join the Afroterps family to stay up to date with upcoming webinars,
      industry news and so much more!
    </p>

    <form
      class="form"
      action="https://afroterps.us6.list-manage.com/subscribe/post?u=f2a143c3e66a5de9414518c65&amp;id=94f84e967f"
      method="post"
      target="_blank"
    >
      <label class="form__item">
        <input
          class="form__input"
          type="text"
          name="FNAME"
          placeholder="Your First Name"
          required
        />
      </label>

      <label class="form__item">
        <input
          class="form__input"
          type="email"
          name="EMAIL"
          placeholder="Your Email"
          required
        />
      </label>
      <button
        class="form__button"
        type="submit"
        value="Subscribe"
        name="subscribe"
      >
        Subscribe
        <i class="fab fa-telegram-plane"></i>
      </button>
    </form>
  </div>
</template>

<script>
// import Form from './form.vue'
export default {
  name: 'Join',
  components: {
    // Form,
  },
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

.form__item {
  width: 100%;
  margin-bottom: 0.5rem;
}

.form__input {
  width: 100%;
  border: 1px solid #916b367c;
  padding: 0.9rem 1.5rem;
  outline: none;
  border-radius: 30px;
  text-align: center;
  color: #432e2dd3;

  @media screen and (max-width: 600px) {
    text-align: left;
  }

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
  border-radius: 30px;
  font-weight: 600;
  font-size: 1rem;
}
</style>
