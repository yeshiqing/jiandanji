<template>
  <ul class="types">
    <li :class="type==='-' && 'selected'" @click="selectType('-')">支出</li>
    <li :class="type==='+' && 'selected'" @click="selectType('+')">收入</li>
  </ul>
</template>

<script lang="ts">
  import Vue from 'vue';
  import {Component} from 'vue-property-decorator';

  @Component
  export default class Types extends Vue {
    type = '-'; // '-' 表示支出，'+'表示收入
    selectType(type: string) { // type 只能是 '-' 和 '+' 中的一个
      if (type !== '-' && type !== '+') {
        throw new Error('unknown value of type');
      }
      this.type = type;
    }
  }
</script>

<style lang="scss" scoped>
  .types {
    background: #c4c4c4;
    display: flex;
    justify-content: center;
    font-size: 24px;

    > li {
      width: 50%;
      height: 64px;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;

      &.selected::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        height: 4px;
        width: 100%;
        background: #333;
      }
    }
  }
</style>