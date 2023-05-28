<template>
  <section class="chat-background">
    <div class="messages">
      <div class="container">
        <div class="block">Анекдоты:</div>
        <div class="block">Возможность регистрации</div>
        <div class="block">Иногда может генерировать неверную информацию</div>
        <div class="block">
          Человеку, потерявшему в Концертном зале "Россия" золотые часы с
          бриллиантами, сообщаем - полвосьмого.
        </div>
        <div class="block">Возможность входа</div>
        <div class="block">
          Иногда может содержать вредные инструкции или предвзятое содержание
        </div>
        <div class="block">Аренда пляжных зонтиков - ночью скидка 10%</div>
        <div class="block">Возможность выхода</div>
        <div class="block">
          Ограниченные знания о мире и событиях после 2021 года
        </div>
      </div>
    </div>

    <div class="interface">
      <textarea
        type="text"
        class="interface-input"
        placeholder="Введите сообщение..."
        disabled
      />
      <button disabled class="btn-chat">Отправить</button>
    </div>
  </section>
</template>

<script>
import MessageReceived from './MessageReceived.vue'
import MessageSentVue from './MessageSent.vue'
export default {
  components: { MessageReceived },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,400;1,500;1,700;1,900&display=swap');
* {
  font-family: 'Roboto';
}

.container {
  max-width: 50vw;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 0.15rem;
  margin: 0 auto;
  padding: 0.2rem;
  margin: 5vw 0 0 16.67vw;
}

.block {
  background-color: #3448af;
  border: 1px solid #d0d5dd;
  color: #fff;
  padding: 0.5rem;
  text-align: center;
  font-size: 1.2rem;
  border-radius: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.chat-background {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height: 94vh;
  /* width: ; */
}
textarea {
  resize: none;
}

.interface {
  position: relative;
}

.interface-input {
  margin-left: 16.67vw;
  box-sizing: border-box;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  gap: 8px;
  padding: 10px;
  width: 50vw;
  height: 128px;
  right: 20vw;
  bottom: 2vh;
  background: #ffffff;
  border: 1px solid #d0d5dd;
  border-radius: 8px;
}
.ajuara-guj {
  position: relative;
}

.btn-chat {
  position: absolute;
  bottom: 5%;
  right: 1%;
  border: none;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-self: flex-start;
  padding: 0;
  color: #fff;
  width: 5.36vw;
  height: 2.08vw;
  background: #3448af;
  border-radius: 5.21vw;
  flex: none;
  align-self: stretch;
  flex-grow: 0;
  font-weight: 500;
  font-size: 0.73vw;
  line-height: 1.04vw;
  margin: 1.25vw auto 0 auto;
}

@media (max-width: 767px) {
  .chat-title {
    display: none;
  }
  .chat {
    margin: 0 auto;
  }
}
</style>
