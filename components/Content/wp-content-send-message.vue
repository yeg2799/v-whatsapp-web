<template lang="pug">
  .content-send-message
    .content-send-message-left
      .content-send-message-icons
        .content-send-message-icon
          SvgSprite(icon="sticker")
        .content-send-message-icon
          SvgSprite(icon="clip")
    .content-send-message-center
      .content-send-message-center-input
        wp-text-field(placeholder="Bir mesaj yazın")
    .content-send-message-right
      .content-send-message-icons
        .content-send-message-icon
          SvgSprite(icon="microphone")
</template>

<script>
import WpTextField from '@/components/TextField/wp-text-field.vue';
export default {
  components: {
    WpTextField,
  }
}
</script>

<style lang="scss" scoped>
  .content-send-message {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 62px;
    background: #202C33;
    color: #fff;
    padding: 10px 16px;
    &-icons {
      display: flex;
    }
    &-center-input {
      .text-field {
        width: 100%;
        background: #2a3942;
      }

    }
  }
</style>
