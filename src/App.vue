<template>
  <div id="money-app">
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import "~@/assets/style/reset.scss";
  @import "~@/assets/style/helper.scss";

  body {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #333;
    line-height: 1.5;
    font-size: 16px;
    font-family: $font-hei;
  }

  .clearfix::after {
    content: '';
    display: block;
    clear: both;
  }

</style>
