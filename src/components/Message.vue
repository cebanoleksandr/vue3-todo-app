<script>
export default {
  emits: ['hide'],
  props: {
    text: String,
  },
  methods: {
    hide() {
      this.$emit('hide');
    },
  }
}
</script>

<template>
  <article
    class="message"
    :class="{ 'message--hidden': !text }"
  >
    <div class="message-header">
      <p>Error</p>
      <button class="delete" @click="hide"></button>
    </div>

    <div class="message-body">
      {{ text }}
    </div>
  </article>
</template>

<style></style>
