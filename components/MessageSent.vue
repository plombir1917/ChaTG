<template>
  <div
    :class="'message-block__sent'"
    :style="{ width: '690px', height: blockHeight }"
  >
    <p class="message-text__sent">{{ text }}</p>
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
.message-block__sent {
  margin: 9vh 50%;
  display: flex;
  justify-content: flex-end;
  width: 35.94vw;

  background: #3448af;
  border-radius: 1.25vw 0 1.25vw 1.25vw;
  height: fit-content;
  padding: 0.83vw 1.25vw;
}

.message-text__sent {
  font-family: Roboto, serif;
  word-wrap: break-word;
  font-weight: 400;
  font-size: 0.83vw;
  line-height: 1.25v;
  color: #fff;
}
</style>
