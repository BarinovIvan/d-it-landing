<template>
  <button @click="$emit('click')">
    <slot />
  </button>
</template>

<script>
  export default {
    name: "AppButton"
  }
</script>

<style lang="scss" scoped>
  button {
    padding: 15px;
    color: white;
    background: #8447E9;
    border: 0;
  }
</style>