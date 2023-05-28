<template>
  <div
    :class="'message-block'"
    :style="{ width: '690px', height: blockHeight }"
  >
    <p class="message-text">{{ text }}</p>
  </div>
</template>
<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      blockHeight: 'auto',
    }
  },
  mounted() {
    this.adjustBlockSize()
  },
  watch: {
    text() {
      this.adjustBlockSize()
    },
  },
  methods: {
    adjustBlockSize() {
      this.$nextTick(() => {
        const block = this.$el.querySelector('#message-block')
        if (block) {
          const maxHeight = 400
          const contentHeight = block.scrollHeight
          const newHeight = Math.min(contentHeight, maxHeight)
          this.blockHeight = `${newHeight}px`
        }
      })
    },
  },
}
</script>
<style scoped>
.message-block {
  margin: 50px auto;
  width: 35.94vw;

  background: #eff1f9;
  border-radius: 0vw 1.25vw 1.25vw 1.25vw;
  height: fit-content;
  padding: 0.83vw 1.25vw;
}

.message-text {
  font-family: Roboto, serif;
  word-wrap: break-word;
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25v;
  color: #000;
}
</style>
