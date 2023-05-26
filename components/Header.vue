<template>
  <div>
    <header
      class="d-flex sticky-top flex-wrap sticky align-items-center justify-content-center justify-content-md-between py-3 border-bottom"
    >
      <div class="col-md-3 mb-2 mb-md-0">
        <a
          href="/"
          class="d-inline-flex link-body-emphasis text-decoration-none"
        >
          <svg
            class="bi"
            width="40"
            height="32"
            role="img"
            aria-label="Bootstrap"
          >
            <use xlink:href="#bootstrap" />
          </svg>
        </a>
      </div>

      <ul class="nav col-12 col-md-auto mb-2 justify-content-center mb-md-0">
        <li>
          <nuxt-link class="nav-link px-2" to="/">Главная</nuxt-link>
        </li>
        <li>
          <nuxt-link class="nav-link px-2" to="/chat">Чат</nuxt-link>
        </li>
      </ul>

      <div class="col-md-3 text-end">
        <nuxt-link to="/login"
          ><button type="button" class="btn btn-outline-primary me-2">
            Войти
          </button></nuxt-link
        >
      </div>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.form-control-dark {
  border-color: var(--bs-gray);
}
.form-control-dark:focus {
  border-color: #fff;
  box-shadow: 0 0 0 0.25rem rgba(255, 255, 255, 0.25);
}

.text-small {
  font-size: 85%;
}

.dropdown-toggle:not(:focus) {
  outline: 0;
}
</style>
