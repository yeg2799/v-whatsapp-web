<template lang="pug">
  .header
    .header-left
      wp-image-card(preset="avatar" src="avatar.jpeg")
    .header-right
      .header-icon
        SvgSprite(icon="status")
      .header-icon
        SvgSprite(icon="chat")
      .header-icon
        SvgSprite(icon="menu")
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 59px;
    background: #202C33;
    color: #fff;
    padding: 10px 16px;
    &-right {
      display: flex;
      align-items: center;
      justify-content: space-between;
      .header-icon{
        cursor: pointer;
        color: #aebac1;
        padding: 8px;
        margin-left: 10px;
        :first-child{
          margin-left: 0;
        }
      }
    }
  }
</style>
