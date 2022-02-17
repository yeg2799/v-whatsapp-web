<template lang="pug">
  nuxt-img(:preset="preset" :src="src" :class="{ 'avatar': preset === 'avatar' }")
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true
    },
    preset: {
      type: String,
      default: ''
    }
  },
}
</script>

<style lang="scss">
.avatar {
  border-radius: 50%;
}
</style>
