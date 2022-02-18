<template lang="pug">
  .sidebar-person-list
    .sidebar-archived-messages
      .sidebar-archived-messages-icon
        SvgSprite(icon="archived")
      .sidebar-archived-messages-text
        span Arşivlenmiş
    .sidebar-messages-list(v-for="a in 10" :key="a")
      .sidebar-messages-person-wrapper
        .sidebar-messages-person-image
          wp-image-card(preset="avatar" src="avatar.jpeg")
        .sidebar-messages-info
          .sidebar-messages-person-name
            span Emre
          .sidebar-messages-person-last-message
            span Merhaba
      .sidebar-messages-person-time
        span 12:00
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .sidebar-person-list {
    background: #111B21;
    color: #fff;
    height: 100%;
    overflow: scroll;
    .sidebar-archived-messages {
      display: flex;
      align-items: center;
      padding: 10px 0px;

      .sidebar-archived-messages-icon {
        color: #00a884;
        padding: 0 16px;
      }
    }
    .sidebar-messages-list {
      width: auto;
      display: flex;
      justify-content: space-between;
      padding: 15px 16px;
      .sidebar-messages-person-wrapper {

        display: flex;
        justify-content: space-between;
        .sidebar-messages-person-image {
          img {
            width: 50px;
            height: 50px;
          }
        }
        .sidebar-messages-info {
          // border-top: 1px solid #3A4A4F;
          margin-left: 25px;
          .sidebar-messages-person-name {
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 5px;
          }
          .sidebar-messages-person-last-message {
            font-size: 12px;
            color: #8696a0;
          }
        }
      }
      .sidebar-messages-person-time {
        font-size: 12px;
        color: #8696a0;
        margin-top: 5px;
      }
    }
  }
</style>
