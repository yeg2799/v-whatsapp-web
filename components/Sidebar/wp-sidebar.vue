<template lang="pug">
  .sidebar
    wp-sidebar-header
    wp-sidebar-notification
</template>

<script>
import WpSidebarHeader from '@/components/Sidebar/wp-sidebar-header.vue';
import WpSidebarNotification from '@/components/Sidebar/wp-sidebar-notification.vue';
export default {
  components: {
    WpSidebarHeader,
    WpSidebarNotification,
  },
}
</script>

<style>

</style>
