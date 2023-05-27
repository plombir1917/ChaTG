<template>
  <input
    class="input"
    :type="type"
    :placeholder="placeholder"
    :name="name"
    :id="id"
  />
</template>

<style scoped>
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
</style>

<script>
export default {
  name: 'Input',
  props: {
    type: String,
    placeholder: String,
    name: String,
    id: String,
  },
}
</script>
