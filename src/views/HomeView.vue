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
        <div class="brands__list brands-list">
          <brands-item
            v-for="item in brandsList"
            :key='brandsList.id'
            :brand-item="item"
            class="brands-list__item"
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
      <section class="stuff">
        <h2 class="title">Наша команда</h2>
        <div class="stuff__list stuff-list">
          <stuff-item
              v-for="stuff in stuffList"
              :stuff-item="stuff"
              :key="stuff.id"
              class="stuff-list__item"
          />
        </div>
      </section>
      <section class="contact">
        <h2 class="title">Мы с вами свяжемся!</h2>
        <contact-form
            v-if="dialogIsShown"
            @closeDialog="dialogIsShown=false"
            @openDialog="dialogIsShown=true"
        />
        <app-button @click="dialogIsShown=true">Оставить контактные данные</app-button>
      </section>
    </div>
  </div>
</template>

<script>
  import AppButton from "@/components/ui/AppButton";
  import BrandsItem from "@/components/BrandsItem";
  import AboutUsItem from "@/components/AboutUsItem";
  import ServiceItem from "@/components/ServiceItem";
  import StuffItem from "@/components/StuffItem";
  import ContactForm from "@/components/ContactForm";

  export default {
    name: 'HomeView',
    components: { ContactForm, StuffItem, ServiceItem, AboutUsItem, BrandsItem, AppButton },
    data() {
      return {
        dialogIsShown: false,
        brandsList: [
          { id: 1, name: 'Zoom', alt: 'Логотип zoom', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-zoom.png' },
          { id: 2, name: 'Севергазбанк', alt: 'Логотип Севергазбанк', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-severgazbank.png' },
          { id: 3, name: 'СПБ Биржа', alt:'Логотип СПБ Биржа', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-spb-birzha.png'  },
          { id: 4, name: 'EFKO', alt:'Логотип EFKO', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-efko.png'  },
          { id: 5, name: 'LEOMAX', alt:'Логотип LEOMAX', imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-leomax.png'  },
          { id: 6, name: 'Virtual', alt:'Логотип VIRUAL', imageLink: 'https://img.freepik.com/premium-vector/virtual-tech-logo-design-templates_24599-397.jpg?w=2000'  },
          { id: 7, name: 'ProBike', alt:'Логотип ProBike', imageLink: 'https://i.otzovik.com/objects/b/1520000/1518559.png'  }
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
            title: 'Поддержка Bitrix24',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://toplogos.ru/images/thumbs/preview-logo-bitrix-24.png'
          },
          {
            id: 2,
            title: 'Поддержка SAP Ariba',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://roi4cio.com/fileadmin/user_upload/sap-ariba.png'
          },
          {
            id: 3,
            title: 'Поддержка 1C ERP Управление производством',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://www.fkassa.ru/upload/iblock/321/toeeigbrhe3jvesx1qu1u6udjxg0ojlm.png'
          },
          {
            id: 4,
            title: 'Поддержка Experium',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://lbsglobal.com/images/text/logo_experium.JPG'
          },
          {
            id: 5,
            title: 'Сервисная и техническая поддержка',
            caption: 'Доходы наших клиентов возрастают в среднем на 10%',
            serviceLevel:'8x5',
            alt:'',
            imageLink: 'https://cdn4.iconfinder.com/data/icons/technical-support/256/96-1024.png'
          },
        ],
        stuffList: [
          {
            id: 1,
            name: 'Шолпов В.У.',
            caption: 'Выбирает техническое решение задачи: предлагает использовать определенные технические рещения. ' +
                'Он же проверяет работу других разработчиков и решает самые сложные или ответственные технические задачи\'',
            position:'Senior разработчик',
            alt:'Фото Шолпова В.У.',
            imageName: 'senior'
          },
          {
            id: 2,
            name: 'Генералов Г.Г.',
            caption: 'Решает бизнес-задачи, которые закрывают конкретную проблему.',
            position:'Middle разработчик',
            alt:'Фото Генералова Г.Г.',
            imageName: 'middle'
          },
          {
            id: 3,
            name: 'Младшев М.В.',
            caption: 'Решает различные технические задачи',
            position:'Junior разработчик',
            alt:'Фото Младшев М.В.',
            imageName: 'junior'
          },
          {
            id: 4,
            name: 'Системов А.А.',
            caption: 'Занимается поддержкой КИС и решает проблемы с АО',
            position:'Системный администратор',
            alt:'Фото Системова А.А.',
            imageName: 'admin'
          },
          {
            id: 5,
            name: 'Мелехов Г.П.',
            caption: 'Отвечает на вопросы, принимает заявки, решает простые технические задачи',
            position:'Диспетчер',
            alt:'',
            imageName: 'dispetcher'
          }
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

  .brands {
    &__list {
      display: flex;
      gap: 10px;
      justify-content: center;
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
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;

    &__item {
      width: calc(100%/3 - 60px/3);
    }
  }

  .stuff {
    &-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;

      &__item {
        width: calc(100%/3 - 200px/5);
      }
    }
  }
</style>
