<template>
  <div>
    <p>Custom Text Input</p>
    <input
        type="text"
        placeholder="Enter custom text here"
        @change="sendEvent"
    />
  </div>
</template>

<script>
export default {
  name: "CustomTextInput",
  emits: ['customChange'],
  methods: {
      sendEvent(event) {
          this.$emit('customChange', event.target.value)
      }
  },
};
</script>

<style lang="scss" scoped></style>
