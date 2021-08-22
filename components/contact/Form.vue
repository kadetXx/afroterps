<template>
  <div class="contact">
    <h1 class="title">We're here</h1>
    <p class="subtitle">
      Our door is always open to you dear colleagues, for a suggestion or
      comment.
    </p>

    <form
      ref="form"
      class="form"
      name="contact"
      method="post"
      action="https://formspree.io/f/moqynblb"
      @submit="submitForm"
    >
      <label class="form__item">
        <small class="form__label">Your Name</small>
        <input class="form__input" type="text" name="name" required />
      </label>

      <label class="form__item">
        <small class="form__label">Your Email</small>
        <input class="form__input" type="email" name="email" required />
      </label>

      <label class="form__item">
        <small class="form__label">Your Message</small>
        <textarea
          rows="10"
          class="form__input"
          type="text"
          name="message"
          required
        />
      </label>

      <button class="form__button" type="submit">
        {{ loading ? '...' : 'Send' }}
      </button>
      <small v-if="success" class="form__message form__message--success"
        >Your message has been sent!</small
      >
      <small v-if="error" class="form__message form__message--error"
        >An error occured, please try again!</small
      >
    </form>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      loading: false,
      success: false,
      error: false,
    }
  },

  watch: {
    success() {
      this.success &&
        setTimeout(() => {
          this.success = false
        }, 5000)
    },

    error() {
      this.error &&
        setTimeout(() => {
          this.error = false
        }, 5000)
    },
  },

  methods: {
    submitForm(ev) {
      ev.preventDefault()

      this.loading = true

      const form = ev.target
      const data = new FormData(form)
      const xhr = new XMLHttpRequest()

      xhr.open(form.method, form.action)
      xhr.setRequestHeader('Accept', 'application/json')

      xhr.onreadystatechange = () => {
        if (xhr.readyState !== XMLHttpRequest.DONE) return
        if (xhr.status === 200) {
          form.reset()
          this.success = true
          this.loading = false
        } else {
          this.loading = false
          this.error = true
        }
      }

      xhr.send(data)
    },
  },
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
  margin-bottom: 0;
}

.subtitle {
  margin-bottom: 3rem;
  color: #442f2e;
  opacity: 0.9;
}

.form {
  display: flex;
  flex-direction: column;
  width: 100%;
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

.form__message {
  text-align: center;
  margin: 1rem 0;
  font-weight: 600;
  font-size: 1rem;

  &--success {
    color: #52b75f;
  }

  &--error {
    color: crimson;
  }
}
</style>
