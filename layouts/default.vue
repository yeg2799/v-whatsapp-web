<template lang="pug">
  .layout
    .left-content
      wp-sidebar
    .right-content
      Nuxt
</template>

<script>
import { onMounted, ref, useContext, watch, onUnmounted, onBeforeMount } from '@nuxtjs/composition-api';
import WpSidebar from '@/components/Sidebar/wp-sidebar.vue';
export default {
  components: {
    WpSidebar
  },
  setup(props, context) {
    const data = ref('emre');
    const heigt = ref(0);
    const contentBodyHeight = ref(0);

    const handleResize = () => {
      console.log('resize');
      const sidebarHeader = document.getElementsByClassName('header')[0];
      const sidebarNotification = document.getElementsByClassName('sidebar-notification')[0];
      const sidebarSearch = document.getElementsByClassName('sidebar-search')[0];
      const personList = document.getElementsByClassName('sidebar-person-list')[0];
      const sumHeight = sidebarHeader.clientHeight + sidebarNotification.clientHeight + sidebarSearch.clientHeight;

      heigt.value = window.innerHeight - sumHeight;

      // const contentHeader = document.getElementsByClassName('content-header')[0];
      // const contentBody = document.getElementsByClassName('content-body')[0];
      // const contentSendMessage = document.getElementsByClassName('content-send-message')[0];
      // const heigt = contentHeader.clientHeight + contentSendMessage.clientHeight;
      // contentBodyHeight.value = window.innerHeight - heigt;

      personList.style.maxHeight = `${heigt.value}px`;
      // contentBody.style.maxHeight = `${contentBodyHeight.value}px`;
      // contentBody.style.height = `${contentBodyHeight.value}px`;
    };
    onBeforeMount(() => {
       window.addEventListener('resize', handleResize);
    });
    onUnmounted(() => {
      window.removeEventListener('resize', handleResize);
    });
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
  height: 100%;
  color: #fff;
  overflow-y: hidden;
  .left-content {
    width: 30%;
    border-right: 1px solid #3A4A4F;

  }
  .right-content {
    width: 70%;
  }
}

</style>
