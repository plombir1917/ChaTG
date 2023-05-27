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
          <Input
            type="email"
            placeholder="Введите вашу почту"
            name="email"
            id="1"
          />
        </div>
        <div class="forms-input">
          <span class="forms-input__label">Пароль</span>
          <Input
            type="password"
            placeholder="Введите пароль"
            name="password"
            id="2"
          />
        </div>
        <div class="forms-input">
          <span class="forms-input__label">Как к вам обращаться</span>
          <Input type="name" placeholder="Введите имя" name="username" id="3" />
        </div>
      </div>
      <Button class="button" name="Зарегистрироваться" />
      <p class="registration-auth">
        Уже есть аккаунт? <nuxt-link to="/login"><a>Войдите</a></nuxt-link>
      </p>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  components: {
    Backgr: () => import('../UI/Backgr.vue'),
    Button: () => import('../UI/Button.vue'),
    Input: () => import('../UI/Input.vue'),
  },
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
a {
  text-decoration: none;
}
.registration {
  font-family: Roboto, serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  isolation: isolate;
  width: 24.17vw;
  height: 28.54vw;
  position: relative;
  left: calc(50% - 24.17vw / 2);
  top: calc(50% - 28.54vw / 2 - 7.5vw);
  background: #ffffff;
  border-radius: 1.67vw;
  margin-top: 6.35vw;
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
