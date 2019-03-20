<template>
  <div class="funny-ebalo"></div>
</template>

<script>
  export default {};
</script>

<style lang="scss">
  .funny-ebalo {
    width: 26px;
    height: 26px;
    background: url("~@/assets/images/sprite.gif");
    background-position: 0px 36px;

    &:active {
      background-position: 118px 36px;
    }

    &:hover {
      cursor: pointer;
    }
  }
</style>
