<template>
  <div class="header">
    <div class="container">
      <h1>Виртуал</h1>
      <nav>
        <router-link to="/">Главная</router-link>
        <router-link to="/">О нас</router-link>
        <router-link to="/">Наши проекты</router-link>
      </nav>
    <app-button>Свяжитесь с нами</app-button>
    </div>
  </div>
</template>

<script>
  import AppButton from "@/components/ui/AppButton";

  export default {
    name: "TheHeader",
    components: { AppButton }
  }
</script>

<style lang="scss" scoped>
  .header .container {
    font-family: "Montserrat", sans-serif;
    display: flex;
    justify-content: space-between;
    align-items: center;

    nav>* {
      margin-right: 50px;
    }
  }
</style>