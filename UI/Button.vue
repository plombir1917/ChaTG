<template>
  <button class="btn">{{ name }}</button>
</template>

<style scoped>
/*  3448AF */
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
</style>

<script>
export default {
  name: 'Button',
  props: {
    name: String,
  },
}
</script>
