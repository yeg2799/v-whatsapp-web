<template lang="pug">
  .sidebar-search
    wp-text-field
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
  .sidebar-search {
    padding: 10px;
    background: #111B21;
    border-bottom: 1px solid #8696a026;
    height: 49px;
  }
</style>
