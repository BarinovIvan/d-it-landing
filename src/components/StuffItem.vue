<template>
  <div class="stuff">
    <img :src="require(`@/assets/stuff/${ stuffItem.imageName }.jpg`)" :alt="stuffItem.alt">
    <h2>{{ stuffItem.name }}</h2>
    <p class="stuff__position">{{ stuffItem.position }}</p>
    <p class="stuff__caption">{{ stuffItem.caption }}</p>
  </div>
</template>

<script>
  export default {
    name: "StuffItem",
    props: {
      stuffItem: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="scss" scoped>
  .stuff {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 10px;

    &__position {
      font-style: italic;
      font-size: 18px;
    }
  }
</style>