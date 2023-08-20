<template>
    <div class="nav-bar d-md-flex pt-6 justify-space-between">
      <div>
        <v-img
        width="40"
        height="40"
        src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
      ></v-img>
      </div>
    
      <div class="nav-link d-flex justify-space-between" :style="$vuetify.theme.themes.myTheme.colors.primary2">
        <v-btn variant="plain" href="/#home">Home</v-btn>
        <v-btn variant="plain" href="/#about">About us</v-btn>
        <v-btn variant="plain" href="/#project">Project</v-btn>
        <v-btn rounded="xl" class="shaded-btn" href="/#contact" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.tertiary2}">Contact us</v-btn>
      </div>
    
      
      <v-menu offset-y v-if="!showBurgerMenu">
        <template v-slot:activator="{ props }">
          <v-btn variant="plain" v-bind="props" style="transform: scale(1.5);"  icon="mdi-menu"></v-btn>
        </template>
        <v-list>
          <v-list-item v-for="(item, index) in menuItems" :key="index">
            <v-btn style="width: 150px;" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}" variant="text">{{ item }}</v-btn>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
    
    </template>
    
    <script>
export default {
  data() {
    return {
      menuItems: ["Home", "About us", "Project", "Contact us"],
      showBurgerMenu: false
    };
  },
  mounted() {

    this.showBurgerMenu = window.innerWidth >= 960;
    // console.log(this.showBurgerMenu)
  
    window.addEventListener("resize", this.updateBurgerMenu);
    console.log(this.showBurgerMenu)
  },
  beforeDestroy() {
    // Remove event listener on component destruction
    window.removeEventListener("resize", this.updateBurgerMenu);
  },
  methods: {
    updateBurgerMenu() {
      this.showBurgerMenu = window.innerWidth >= 960;
    }
  }
};
</script>


    <style>
    .nav-bar{
      height: 100px;
      padding:0  7%;
    }
    .nav-link{
      width: 500px;
     font-size: 16px;
      font-weight: 600;
    }
    .shaded-btn{
      color: white !important;
      font-size: 16px;
      font-weight: 600;
      width: 130px;
      height: 49px;
    }
    @media (max-width: 960px) {
  .nav-link {
    display: none !important;
  }
  .nav-bar{
    display: flex;
  }
  
}
    </style>