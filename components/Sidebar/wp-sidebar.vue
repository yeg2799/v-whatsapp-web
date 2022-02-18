<template lang="pug">
  .sidebar
    wp-sidebar-header
    wp-sidebar-notification
    wp-sidebar-search
    wp-sidebar-person-list
</template>

<script>
import WpSidebarHeader from '@/components/Sidebar/wp-sidebar-header.vue';
import WpSidebarNotification from '@/components/Sidebar/wp-sidebar-notification.vue';
import WpSidebarSearch from '@/components/Sidebar/wp-sidebar-search.vue';
import WpSidebarPersonList from '@/components/Sidebar/wp-sidebar-person-list.vue';
export default {
  components: {
    WpSidebarHeader,
    WpSidebarNotification,
    WpSidebarSearch,
    WpSidebarPersonList
  },
}
</script>

<style>

</style>
