<template lang="pug">
  .sidebar-notification
    .left-notification-content
      .notification-icon
        SvgSprite(icon="alert-notification")
    .right-notification-content
      span Yeni mesaj geldiğinde bildirim alın
      .notification-content
        span Masaüstü bildirimlerini aç
        .chevron-icon
          SvgSprite(icon="chevron-right")
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .sidebar-notification {
    display: flex;
    align-items: center;
    background: #182229;
    padding: 13px 12px 14px 13px;
    color: #fff;

    .left-notification-content {
      margin-right: 15px;
      .notification-icon {
        color: #53BDEB;
        display: inline-block;
    }
    }

    .right-notification-content{
      display: flex;
      flex-direction: column;
      .notification-content {
        display: flex;
        flex-direction: row;
        align-items: center;
        color: #8696a0;
        cursor: pointer;
        &:hover {
          text-decoration:underline;
          text-decoration-color: #8696a0;
        }
        .chevron-icon {
          margin-left: 3px;
        }

      }
    }
  }
</style>
