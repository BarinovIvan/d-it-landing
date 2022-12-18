<template>
  <div class="service-item">
    <img :src="serviceItem.imageLink" :alt="serviceItem.alt"/>
    <h2>{{ serviceItem.title }}</h2>
    <p>{{ serviceItem.caption }}</p>
    <p class="service-item__service-level">Уровень сервиса: {{ serviceItem.serviceLevel }}</p>
  </div>
</template>

<script>
  export default {
    name: "ServiceItem",
    props: {
      serviceItem: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="scss" scoped>
  .service-item{
    display: flex;
    justify-content: left;
    align-items: center;
    flex-direction: column;
    width: fit-content;
    padding: 10px;
    box-sizing: border-box;
    box-shadow: 0 0 10px rgba(65, 64, 64, 0.78);
    border-radius: 10px;

    &__service-level{
      font-weight: 600;
    }

    img {
      height: 144px;
    }

    h2 {
      font-size: 20px;
      color: #8447E9;
    }

    & > * {
      margin-bottom: 20px;
    }
  }
</style>