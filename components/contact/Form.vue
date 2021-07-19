<template>
  <div class="contact">
    <h1 class="title">Contact Us</h1>

    <form class="form">
      <label class="form__item">
        <small class="form__label">Your Name</small>
        <input class="form__input" type="text" name="name" />
      </label>

      <label class="form__item">
        <small class="form__label">Your Email</small>
        <input class="form__input" type="text" name="name" />
      </label>

      <label class="form__item">
        <small class="form__label">Your Name</small>
        <textarea rows="10" class="form__input" type="text" name="name" />
      </label>

      <button class="form__button" type="submit">Send</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Form',
}
</script>

<style lang="scss" scoped>
.contact {
  min-height: 100vh;
  padding: 2rem 15% 4rem 5%;

   @media screen and (max-width: 600px) {
    padding: 2rem 5% 4rem 5%;
  }
}

.title {
  margin-bottom: 2rem;
}

.form {
  display: flex;
  flex-direction: column;
}

.form__item {
  display: flex;
  flex-direction: column;
  margin-block: 0.5rem;
}

.form__label {
  color: #442f2e;
  font-size: 1rem;
  opacity: 0.7;
  margin-bottom: 0.3rem;
}

.form__input {
  padding: 0.8rem;
  outline: none;
  border: 1px solid #442f2e31;
  border-radius: 4px;
}

.form__button {
  padding: 0.8rem;
  margin-top: 0.5rem;
  background: #442f2e;
  color: #fff;
  outline: none;
  border: none;
  border-radius: 4px;
  font-size: 1.1rem;
  font-weight: 600;
}
</style>
