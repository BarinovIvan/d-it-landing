<template>
  <div class="home">
    <div class="container">
      <section class="hello">
        <h1 class="hello__title">
          Мы поможем вам наладить ИТ-инфраструктуру
        </h1>
        <app-button>Ознакомтесь с нашим сервисом</app-button>
      </section>
      <section class="brands">
        <h2 class="title">Мы работаем с этими брендами</h2>
        <div class="brands__list">
          <brands-item
            v-for="item in brandsList"
            :key='brandsList.id'
            :brand-item="item"
          />
        </div>
      </section>

    </div>
  </div>
</template>

<script>
  import AppButton from "@/components/ui/AppButton";
  import BrandsItem from "@/components/BrandsItem";
  export default {
    name: 'HomeView',
    components: {BrandsItem, AppButton },
    data() {
      return {
        brandsList: [
          {id: 1, name: 'Битрикс24', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'}
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .hello {
    &__title {
      font-size: 50px;
      font-weight: 600;
      margin-bottom: 2.5%;
    }
  }

  .brands .title {
    margin-bottom: 20px;
  }
</style>
