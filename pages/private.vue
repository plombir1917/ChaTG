<template>
  <section>
    <Backgr />
    <div class="auth">
      <nuxt-link to="/logged">
        <img
          src="../static/closeIcon.svg"
          alt="closeIcon"
          class="auth-close__icon"
        />
      </nuxt-link>
      <img src="../static/post.svg" alt="auth-logo" class="auth-logo" />
      <p class="auth-name">Почта России GPT</p>
      <p class="auth-hello">Личный кабинет</p>
      <div class="authInfo__label">
        <span>Ваше имя</span>
        <p>Username</p>
        <span>Ваша почта</span>
        <p>*тут почта пользователя*</p>
        <span>Пароль</span>
        <p>*******</p>
      </div>
      <button class="btn" @click="logout">Выйти</button>
    </div>
  </section>
</template>
<script>
export default {
  methods: {
    logout() {
      this.$store.dispatch('logout')
      this.$router.push('/')
    },
  },
  components: {
    Backgr: () => import('../UI/Backgr.vue'),
  },
}
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.auth {
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

.auth-close__icon {
  position: absolute;
  top: 0.83vw;
  right: 0.83vw;
  background: none;
  border: none;
  outline: none;
  cursor: pointer;
  z-index: 1;
}

.auth-name {
  font-weight: 600;
  font-size: 1.56vw;
  line-height: 2.08vw;
  color: #000000;
  margin: 0.21vw 0 0.21vw 0;
}

.auth-logo {
  width: 4.27vw;
  height: 2.08vw;
  margin-top: 2.08vw;
}

.auth-hello {
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  margin-bottom: 1.25vw;
}

.authInfo__label {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  font-weight: 500;
  font-size: 0.73vw;
  line-height: 1.04vw;
  color: #000000;
}
.authInfo__label p {
  padding-bottom: 1vw;
}
.auth-auth {
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25vw;
  /* margin: 0 0 2.08vw 0; */
  margin: 0.5vw 0 2vw 0;
  color: #667085;
}

.auth-auth a {
  color: #3448af !important;
  cursor: pointer;
}

.btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0;
  color: #fff;
  width: 13.33vw;
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

@media (max-width: 1120px) {
  .auth {
    overflow: scroll;
  }
}
</style>
