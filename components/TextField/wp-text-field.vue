<template lang="pug">
  .text-field
    .text-field-icon
      SvgSprite(icon="search")
    .text-field-input
      input(type="text" placeholder="Aratın veya yeni bir sohbet başlatın")
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .text-field {
    display: flex;
    align-items: center;
    border: 1px solid transparent;
    border-radius: 8px;
    background: #202C33;
    position: relative;
    .text-field-icon {
      color: #8696a0;
      display: inline-block;
      margin-right: 30px;
    }
    .text-field-input {
      width: 100%;
      input {
        width: 100%;
        // height: 35px;
        border: none;
        background: transparent;
        color: #8696a0;
        font-size: 14px;

        &:focus {
          outline: none;
        }
      }
    }
  }
</style>
