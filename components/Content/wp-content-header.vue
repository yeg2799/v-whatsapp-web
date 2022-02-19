<template lang="pug">
  .content-header
    .content-header-left
      .content-header-left-image
        wp-image-card(preset="avatar" src="https://st2.depositphotos.com/3557671/11164/v/950/depositphotos_111644750-stock-illustration-man-avatar-icon-of-vector.jpg")
      .content-header-left-name
        span Berat
    .content-header-right
      .content-header-right-icon
        SvgSprite(icon="search")
      .content-header-right-icon
        SvgSprite(icon="menu")
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.content-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 59px;
    background: #202C33;
    color: #fff;
    padding: 10px 16px;
    &-left {
      display:flex;
      align-items:center;
      &-image {
        margin-right: 15px;
      }
    }
    &-right {
      display: flex;
      align-items: center;
      justify-content: space-between;
      .content-header-right-icon{
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
