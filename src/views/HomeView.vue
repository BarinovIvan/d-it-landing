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
      <section class="AboutUs">
        <h2 class="title">Наше агенство обеспечит вас всеми необходимыми услугами</h2>
        <div class="aboutUsList">
          <about-us-item
            v-for="item in aboutUsList"
            :key="item.id"
            :aboutItem="item"
            class="aboutUsList__item"
          />
        </div>
      </section>
      <section class="services">
        <h2 class="title">
          Наши услуги
        </h2>
        <div class="services__list services-list">
          <service-item
            v-for="item in servicesList"
            :key="item.id"
            :serviceItem="item"
            class="services-list__item"
          />
        </div>
      </section>
    </div>
  </div>
</template>

<script>
  import AppButton from "@/components/ui/AppButton";
  import BrandsItem from "@/components/BrandsItem";
  import AboutUsItem from "@/components/AboutUsItem";
  import ServiceItem from "@/components/ServiceItem";
  export default {
    name: 'HomeView',
    components: {ServiceItem, AboutUsItem, BrandsItem, AppButton },
    data() {
      return {
        brandsList: [
          { id: 1, name: 'Битрикс24', alt:'', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'  }
        ],
        aboutUsList: [
          { id: 1, title: 'С нами ваш доход увеличится', caption: 'Доходы наших клиентов возрастают в среднем на 10%', imageName: 'Icon1' },
          { id: 2, title: 'Множество клиентов', caption: 'Поможем привлечь новых клиентов в вашу компанию', imageName: 'Icon2' },
          { id: 3, title: '6 лет на рынке', caption: 'Наша компания активно развивается уже 6 лет', imageName: 'Icon3' },
          { id: 4, title: 'Обеспечиваем постоянный сервис', caption: 'Доступны 7 дней в неделю', imageName: 'Icon4' }
        ],
        servicesList: [
          {
            id: 1,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 2,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 3,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 4,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 5,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 6,
            title: 'С нами ваш доход увеличится',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .home {
    font-family: "Montserrat", sans-serif;
  }

  .hello {
    &__title {
      font-size: 50px;
      font-weight: 600;
      margin-bottom: 2.5%;
    }
  }

  .aboutUsList {
    display: flex;
    justify-content: space-between;

    &__item {
      width: calc(100%/4 - 60px/3);
    }
  }

  .services-list {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;

    &__item {
      width: calc(100%/3 - 60px/3);
    }
  }
</style>
