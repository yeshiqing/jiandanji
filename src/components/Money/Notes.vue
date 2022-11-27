<template>
  <div>
    <label class="notes">
      <span class="name">备注</span>
      <input class="addNotes" placeholder="点此输入备注...">
    </label>
  </div>
</template>

<script lang="ts">
  export default {
    name: 'Notes'
  };
</script>

<style lang="scss" scoped>
  .notes {
    font-size: 14px;
    background: #f5f5f5;
    display: block;
    padding: 0 16px;

    .name {
      padding-right: 16px;
    }

    input {
      height: 64px;
      border: none;
      background: transparent;
    }
  }
</style>