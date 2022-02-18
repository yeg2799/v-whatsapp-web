<template lang="pug">
  .content
    wp-content-header
    wp-content
    wp-content-send-message
</template>

<script>
import { onMounted, ref, useContext, watch, onUnmounted, onBeforeMount } from '@nuxtjs/composition-api';
import WpContentHeader from '@/components/Content/wp-content-header.vue';
import WpContent from '@/components/Content/wp-content.vue';
import WpContentSendMessage from '@/components/Content/wp-content-send-message.vue';
export default {
  name: 'IndexPage',
  components: {
    WpContentHeader,
    WpContent,
    WpContentSendMessage
  },
  setup() {
    const personListHeight = ref(0);
    const contentBodyHeight = ref(0);

    const handleResize = () => {
      console.log('resize');
      const sidebarHeader = document.getElementsByClassName('header')[0];
      const sidebarNotification = document.getElementsByClassName('sidebar-notification')[0];
      const sidebarSearch = document.getElementsByClassName('sidebar-search')[0];
      const personList = document.getElementsByClassName('sidebar-person-list')[0];
      const sumHeight = sidebarHeader.clientHeight + sidebarNotification.clientHeight + sidebarSearch.clientHeight;

      personListHeight.value = window.innerHeight - sumHeight;

      const contentHeader = document.getElementsByClassName('content-header')[0];
      const contentBody = document.getElementsByClassName('content-body')[0];
      const contentSendMessage = document.getElementsByClassName('content-send-message')[0];
      const heigt = contentHeader.clientHeight + contentSendMessage.clientHeight;
      contentBodyHeight.value = window.innerHeight - heigt;

      personList.style.maxHeight = `${personListHeight.value}px`;
      contentBody.style.maxHeight = `${contentBodyHeight.value}px`;
      contentBody.style.height = `${contentBodyHeight.value}px`;
    };
    onMounted(() => {
       window.addEventListener('resize', handleResize);
       handleResize();
    });
    onUnmounted(() => {
      window.removeEventListener('resize', handleResize);
    });
  }
}
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  flex-direction: column;
  height: 100%;
}
</style>
