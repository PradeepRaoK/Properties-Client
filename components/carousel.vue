<template>
    <div class="carousel">
      <div class="header">
        <v-text>Scroll</v-text>
        <v-icon icon="mdi-menu-down"></v-icon>
      </div>
      <v-carousel cycle interval="3000">
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src" cover
        ></v-carousel-item>
      </v-carousel>
    </div>
  </template>
  

<script>
export default {
  data() {
    return {
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
        }
      ]
    }
  }
}
</script>

<style scoped>
.header{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    animation: float 5s ease-in-out infinite;
    margin-top: 20px 0;
}
  @keyframes float {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-5px);
    }
    100% {
      transform: translateY(0px);
    }
  }
  

</style>