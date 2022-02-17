<template lang="pug">
  .layout
    .left-content
      wp-sidebar
    .right-content
      Nuxt
</template>

<script>
import { ref } from '@nuxtjs/composition-api';
import WpSidebar from '@/components/Sidebar/wp-sidebar.vue';
export default {
  components: {
    WpSidebar
  },
  setup() {
    const data = ref('emre');
    return {
      data
    }
  }
}
</script>

<style lang="scss">
* {
    margin: 0px;
    padding: 0px;
    &,
    &:before,
    &:after {
      box-sizing: border-box;
    }
  }

  *,
  *:focus {
    outline: none;
  }

  html {
    box-sizing: border-box;
    text-rendering: optimizeLegibility;
    position: relative;
    overflow-x: hidden;
  }

  body {
    overflow-x: hidden !important;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
    background: #f7f7f7;
    color: #393c3e;
    font-size: 14px;
  }

.layout {
  display: flex;
  width: 100%;
  .left-content {
    width: 30%;
    border-right: 1px solid #e6e6e6;
  }
  .right-content {
    width: 70%;
  }
}

</style>
