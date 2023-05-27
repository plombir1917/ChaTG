<template>
  <section class="chat-background">
    <span class="chat-title">Начните печатать ниже...</span>
    <div class="interface">
      <textarea
        type="text"
        class="interface-input"
        placeholder="Введите сообщение..."
      />
      <button class="btn">Отправить</button>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,500;0,700;0,900;1,400;1,500;1,700;1,900&display=swap');
textarea {
  resize: none;
}
@media (max-width: 767px) {
  .chat-title {
    display: none;
  }
  .chat {
    margin: 0 auto;
  }
}
.interface-input {
  box-sizing: border-box;

  /* Auto layout */

  display: flex;
  flex-direction: row;
  align-items: flex-end;
  gap: 8px;
  padding: 10px;
  width: 50vw;
  height: 128px;
  right: 20vw;
  bottom: 2vh;

  /* Primary/White */

  background: #ffffff;
  /* Primary/Stroke Gray */

  border: 1px solid #d0d5dd;
  border-radius: 8px;
}
.chat:focus {
  border: 1px solid #3448af;
  border-radius: 8px;
}
.chat-button {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */
  position: relative;
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
.chat-title {
  margin-top: 48.15vh;
  width: 363px;
  height: 40px;
  left: calc(50% - 363px / 2 + 159.5px);
  top: calc(50% - 40px / 2);

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
.chat-background {
  display: flex;
  flex-direction: column;
  margin-left: 320px;
  justify-content: space-between;
  align-items: center;
  height: 94vh;
}
.btn {
  position: absolute;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 8px;
  width: 103px;
  height: 40px;

  /* Blue/Blue */

  background: #3448af;
  border-radius: 100px;

  /* Inside auto layout */
  color: #ffffff;
  flex: none;
  order: 1;
  flex-grow: 0;
}
</style>
