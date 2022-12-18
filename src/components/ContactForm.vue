<template>
  <div class="form__wrapper" @click="$emit('closeDialog')">
    <form class="contact-form" @click.stop>
      <label for="name">Ваше имя и фамилия</label>
      <input name="name" type="text" placeholder="Алексей Валерьевич Дружков">
      <label for="name">Компания</label>
      <input name="name" type="text" placeholder="Рога и копыта">
      <label for="name">Email</label>
      <input name="name" type="email" placeholder="something@gmail.com">
      <label for="name">Телефон</label>
      <input name="name" type="text" placeholder="+79995444466">
      <textarea/>
      <app-button @click="$emit(openDialog)">Связаться</app-button>
    </form>
  </div>
</template>

<script>
  import AppButton from "@/components/ui/AppButton";
  export default {
    name: "ContactForm",
    components: {AppButton}
  }
</script>

<style lang="scss" scoped>
  .form__wrapper {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(0, 0, 0, 0.48);
  }

  .contact-form {
    display: flex;
    flex-direction: column;
    width: 40%;
    padding: 25px;
    border: 1px solid #2c3e50;
    border-radius: 5px;
    background: white;

    input,
    textarea {
      padding: 15px 5px;
      margin: 10px 0 20px;
    }

    button {
      width: 50%;
      margin: 0 auto;
    }
  }
</style>