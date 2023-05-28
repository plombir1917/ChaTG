<template>
  <section class="chat-background">
    <span class="chat-title" v-if="!messageSent">Начните печатать ниже...</span>

    <div class="roof"></div>
    <div class="messages">
      <MessageSent :text="messageSent" v-if="messageSent" />
      <MessageReceived :text="res" v-if="messageSent" />
    </div>

    <div class="interface">
      <textarea
        type="text"
        class="interface-input"
        placeholder="Введите сообщение..."
        v-model="text"
      />
      <button class="btn-chat" @click="onSubmit">Отправить</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      text: '',
      messageSent: '',
    }
  },
  methods: {
    onSubmit() {
      this.messageSent = this.text
    },
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,400;1,500;1,700;1,900&display=swap');
* {
  font-family: 'Roboto';
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
.chat-title {
  margin-top: 48.15vh;
  width: 363px;
  height: 40px;
  margin-right: -25vw;

  /* 30-40, SemiBold */

  font-family: 'Roboto';
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 40px;
  /* identical to box height, or 133% */

  /* Primary/Gray */

  color: #667085;
}
.interface {
  position: relative;
}
.roof {
  position: absolute;
  width: 77%;
  height: 80px;
  left: 320px;
  top: 0px;

  background: linear-gradient(180deg, #ffffff 0%, rgba(255, 255, 255, 0) 100%);
}

.interface-input {
  margin-left: 320px;
  border: 1px solid red;
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
.btn-chat:hover {
  background: #20349b;
  color: #fff;
}

@media (max-width: 767px) {
  .chat-title {
    display: none;
  }
  .chat {
    margin: 0 auto;
  }
}
@media (max-width: 1000px) {
  .interface-input {
    margin: 0;
  }
}
</style>
