<template>
  <div>
    <backgr />
    <section class="registration">
      <nuxt-link to="/">
        <img
          src="../static/closeIcon.svg"
          alt="closeIcon"
          class="registration-close__icon"
      /></nuxt-link>

      <img src="../static/post.svg" alt="registr-logo" class="registr-logo" />
      <p class="registr-name">Почта России GPT</p>
      <p class="registr-hello">Добро пожаловать</p>
      <div class="forms">
        <div class="forms-input">
          <span class="forms-input__label">Электронная почта</span>
          <input
            type="email"
            placeholder="Введите вашу почту"
            name="email"
            id="1"
            class="input"
            v-model="form.email"
          />
        </div>
        <div class="forms-input">
          <span class="forms-input__label">Пароль</span>
          <input
            type="password"
            placeholder="Введите пароль"
            name="password"
            id="2"
            class="input"
            v-model="form.password"
          />
        </div>
        <div class="forms-input">
          <span class="forms-input__label">Как к вам обращаться</span>
          <input
            type="name"
            placeholder="Введите имя"
            name="username"
            id="3"
            class="input"
            v-model="form.name"
          />
        </div>
      </div>
      <button class="button btn" @click="onSubmit">Зарегистрироваться</button>
      <p class="registration-auth">
        Уже есть аккаунт? <nuxt-link to="/login"><a>Войдите</a></nuxt-link>
      </p>
      <b-card class="mt-3" header="Form Data Result">
        <pre class="m-0">{{ form }}</pre>
      </b-card>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: '',
        password: '',
        name: '',
      },
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
  },
  name: 'Modal',
  components: {
    Backgr: () => import('../UI/Backgr.vue'),
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,400;1,500;1,700;1,900&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
span {
  display: block;
}
.input {
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0.52vw 0.83vw;
  gap: 0.42vw;
  width: 20vw;
  height: 2.29vw;
  background: #ffffff;
  border: 0.05vw solid #d0d5dd;
  border-radius: 0.42vw;
  flex: none;
  order: 0;
  flex-grow: 1;
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  margin: 0.21vw 0 0.42vw 0;
}
.login {
  font-family: Roboto, serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  isolation: isolate;
  width: 24.17vw;
  height: 24.79vw;
  position: relative;
  left: calc(50% - 24.17vw / 2);
  top: calc(50% - 28.54vw / 2 - 7.5vw);
  background: #ffffff;
  border-radius: 1.67vw;
  margin-top: 6.35vw;
}
.btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0;
  color: #fff;
  width: 20vw;
  height: 2.08vw;
  background: #3448af;
  border-radius: 5.21vw;
  flex: none;
  align-self: stretch;
  flex-grow: 0;
  z-index: 2;
  font-weight: 500;
  font-size: 0.73vw;
  line-height: 1.04vw;
  margin: 1.25vw auto 0 auto;
}
.btn:hover {
  background: #20349b;
  color: #fff;
}
.registration {
  font-family: Roboto, serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  isolation: isolate;
  width: 24.17vw;
  height: 28.54vw;
  position: absolute;
  left: calc(50% - 24.17vw / 2);
  top: calc(50% - 28.54vw / 2 - 7.5vw);
  background: #ffffff;
  border-radius: 1.67vw;
  margin-top: 6.35vw;
  z-index: 100;
}

.registration-close__icon {
  position: absolute;
  top: 0.83vw;
  right: 0.83vw;
  background: none;
  border: none;
  outline: none;
  cursor: pointer;
  z-index: 1;
}

.registr-name {
  font-weight: 600;
  font-size: 1.56vw;
  line-height: 2.08vw;
  color: #000000;
  margin: 0.21vw 0 0.21vw 0;
}

.registr-logo {
  width: 4.27vw;
  height: 2.08vw;
  margin-top: 2.08vw;
}

.registr-hello {
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  margin-bottom: 1.25vw;
}

.forms-input__label {
  font-weight: 500;
  font-size: 0.73vw;
  line-height: 1.04vw;
  color: #000000;
}

.registration-auth {
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  /* margin: 0 0 2.08vw 0; */
  margin: 0.5vw 0 2vw 0;
  color: #667085;
}

.registration-auth a {
  color: #3448af !important;
  cursor: pointer;
}

@media (max-width: 1120px) {
  .registration {
    overflow: scroll;
  }
}
</style>
