<template>
  <!--Main Navigation-->
  <section>
    <!-- Sidebar -->
    <nav id="sidebarMenu" class="d-lg-block sidebar bg-white">
      <div class="position-sticky">
        <div class="header">
          <nuxt-link to="/">
            <img src="../static/brand.svg" alt="" class="header-brand" />
          </nuxt-link>
          <nuxt-link to="/" class="zero">
            <div class="list-group">
              <img src="../static/icon.svg" alt="" />
              <span>{{ chatName }}</span>
            </div></nuxt-link
          >
        </div>
        <footer>
          <nuxt-link to="/" class="footer-new-button">
            + Создать новый чат</nuxt-link
          >
          <nuxt-link class="footer-link zero" to="/login">
            <img src="../static/user.svg" alt="" class="footer-img" />
            <span class="zero footer-link-text">Выполнить вход</span>
          </nuxt-link>
        </footer>
      </div>
    </nav>
  </section>
</template>

<script>
export default {
  data() {
    return {
      chatName: 'Название чата',
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,400;1,500;1,700;1,900&display=swap');
@media (min-width: 991.98px) {
  main {
    padding-left: 240px;
  }
}

.zero {
  background: none;
  color: none;
  text-decoration: none;
  outline: none;
  color: none;
  border: none;
  text-decoration: none;
}

.header-brand {
  width: 115px;
  height: 56px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0 0 16px 32px;
}
/* Sidebar */
.sidebar {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  padding: 32px 0 0; /* Height of navbar */
  box-shadow: 0 2px 5px 0 rgb(0 0 0 / 5%), 0 2px 10px 0 rgb(0 0 0 / 5%);
  width: 320px;
}
.roof {
  position: absolute;
  width: 100%;
  height: 80px;
  left: 320px;
  top: 0px;

  background: linear-gradient(180deg, #ffffff 0%, rgba(255, 255, 255, 0) 100%);
}

@media (max-width: 991.98px) {
  .sidebar {
    width: 100%;
  }
}
.sidebar .active {
  border-radius: 5px;
  box-shadow: 0 2px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
}

.sidebar-sticky {
  position: relative;
  top: 0;
  height: calc(100vh - 48px);
  padding-top: 0.5rem;
  overflow-x: hidden;
  overflow-y: auto; /* Scrollable contents if viewport is shorter than content. */
}
.list-group {
  position: relative;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 12px 8px;
  gap: 8px;

  width: 256px;
  height: 48px;

  /* Blue/Light Blue */

  background: #eff1f9;
  border-radius: 8px;

  /* Inside auto layout */

  order: 0;
  align-self: stretch;
  margin-left: 1vw;
}
.list-group:hover {
  background-color: #d0d5dd;
}
span {
  width: 208px;
  height: 24px;

  /* 16-24, Regular */

  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  /* identical to box height, or 150% */

  /* Primary/Black */

  color: #000000;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 1;
}
.login-link {
  width: 110px;
  height: 20px;

  /* 14-20, Regular */

  font-family: 'Roboto';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  display: flex;
  align-items: center;
  text-align: center;

  /* Blue/Blue */

  color: #3448af;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
}
.login-link:hover {
  color: cornflowerblue;
}
footer {
  box-sizing: border-box;

  /* Auto layout */

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 24px 32px 32px;
  gap: 10px;

  width: 320px;
  height: 146px;

  /* Primary/Stroke Gray */

  border-top: 1px solid #d0d5dd;

  /* Inside auto layout */

  flex: none;
  order: 1;
  align-self: stretch;
  flex-grow: 0;
  margin: 60vh 0 0 0;
}
.footer-item {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 16px 10px 12px;
  gap: 8px;

  width: 162px;
  height: 40px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
}
.footer-img {
  width: 16px;
  height: 16px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
}
.footer-link {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 16px 10px 12px;
  gap: 8px;

  width: 162px;
  height: 40px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
}
.footer-new-button {
  text-decoration: none;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0px;
  gap: 8px;

  width: 256px;
  height: 40px;

  /* Blue/Blue */

  background: #3448af;
  border-radius: 100px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  align-self: stretch;
  flex-grow: 0;
  color: #ffffff;
}
.footer-new-button:hover {
  background: #20349b;
  color: #fff;
}
.footer-link-text {
  width: 110px;
  height: 20px;

  /* 14-20, Regular */

  font-family: 'Roboto';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  display: flex;
  align-items: center;
  text-align: center;

  /* Blue/Blue */

  color: #3448af;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
}
.footer-link-text:hover {
  color: #20349b;
}
@media (max-width: 1000px) {
  footer {
    margin: 0;
  }
}
</style>
