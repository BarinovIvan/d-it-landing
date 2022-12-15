<template>
  <div class="brands__item">
    <img :src="brandItem.imageLink" alt="Логотип Битрикс 24"/>
    <p>{{ brandItem.name }}</p>
  </div>
</template>

<script>
  export default {
    name: "BrandsItem",
    props: {
      brandItem: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="scss" scoped>
  .brands__item {
      display: flex;
      align-items: center;
      border: 2px solid #A1AEBF;
      width: fit-content;
      padding: 0 10px;
      border-radius: 10px;

    img {
      width: 80px;
      margin-right: 20px;
    }

    p {
      font-weight: 600;
    }
  }
</style>