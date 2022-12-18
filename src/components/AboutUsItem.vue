<template>
  <div class="about-us__item">
    <img :src="require(`@/assets/aboutUs/${aboutItem.imageName}.png`)" alt="Иконка"/>
    <h2>{{ aboutItem.title }}</h2>
    <p>{{ aboutItem.caption }}</p>
  </div>
</template>

<script>
  export default {
    name: "AboutUsItem",
    props: {
      aboutItem: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="scss" scoped>
  .about-us__item{
    display: flex;
    align-items: left;
    justify-content: left;
    flex-direction: column;
    gap: 25px;
    text-align: left;
    width: fit-content;

    h2 {
      font-size: 20px;
      color: #8447E9;
    }

    img {
      width: 144px;
      height: 144px;
    }
  }
</style>