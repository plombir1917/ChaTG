<template>
  <div>
    <Backgr />
    <section class="login">
      <nuxt-link to="/">
        <img
          src="../static/closeIcon.svg"
          alt="closeIcon"
          class="login-close__icon"
        />
      </nuxt-link>

      <img src="../static/post.svg" alt="login-logo" class="login-logo" />
      <p class="login-name">Почта России GPT</p>
      <p class="login-hello">Добро пожаловать</p>
      <form class="forms">
        <div class="forms-input">
          <span class="forms-input__label">Электронная почта</span>
          <input
            type="email"
            placeholder="Введите вашу почту"
            name="email"
            id="1"
            v-model="form.email"
            class="input"
          />
        </div>
        <div class="forms-input">
          <span class="forms-input__label">Пароль</span>
          <input
            type="password"
            placeholder="Введите пароль"
            name="password"
            id="2"
            v-model="form.password"
            class="input"
          />
        </div>
      </form>

      <button class="button btn" name="Войти" @click="onSubmit">Войти</button>

      <p class="login-auth">
        Нет аккаунта?
        <nuxt-link to="/signup"><a>Зарегистрироваться</a></nuxt-link>
      </p>
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
      },
    }
  },

  methods: {
    onSubmit(event) {
      event.preventDefault()
      this.$store.dispatch('login')
      this.$router.push('/logged')
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
  font-family: Roboto;
}
span {
  display: block;
}
a {
  text-decoration: none;
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
  position: absolute;
  left: calc(50% - 24.17vw / 2);
  top: calc(50% - 28.54vw / 2 - 7.5vw);
  background: #ffffff;
  border-radius: 1.67vw;
  margin-top: 6.35vw;
  z-index: 100;
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
.login-close__icon {
  position: absolute;
  top: 0.83vw;
  right: 0.83vw;
  background: none;
  border: none;
  outline: none;
  cursor: pointer;
  z-index: 1;
}

.login-name {
  font-weight: 600;
  font-size: 1.56vw;
  line-height: 2.08vw;
  color: #000000;
  margin: 0.21vw 0 0.21vw 0;
}

.login-logo {
  width: 4.27vw;
  height: 2.08vw;
  margin-top: 2.08vw;
}

.login-hello {
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

.login-auth {
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  margin: 0.5vw 0 2vw 0;
  color: #667085;
}

.login-auth a {
  color: #3448af !important;
  cursor: pointer;
}

@media (max-width: 1120px) {
  .login {
    overflow: scroll;
  }
}
</style>
