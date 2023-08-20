<template>
 <div class="main-header" id="home">
  <v-row >
    <v-col class="main-col1" cols="12" md="7" sm="12">
      <v-text style="font-size: 24px;font-weight: 700;">Welcome to</v-text>
      <v-text style="font-size: 48px;font-weight: 700;">Someshwar Vista</v-text>
      <v-text style="font-size: 16px;font-weight: 400;">Experience life beyond the ordinary</v-text>
    </v-col>
    <v-col class="main-col2" cols="12" md="5" sm="12">
      <v-text style="font-size: 16px;font-weight: 400;">Lorem ipsum dolor sit amet consectetur. Morbi metus libero vulp
        utate habitant morbi diam in molestie.
         Consectetur risus natoque velit nullam curabitur et tincidunt. </v-text>
      <v-btn style="max-width:200px;height: 45px;" :style="{color:$vuetify.theme.themes.myTheme.colors.tertiary2,borderColor:$vuetify.theme.themes.myTheme.colors.tertiary2}" rounded="xl" variant="outlined" class="main-btn" href="#gallery">View gallery</v-btn>
      </v-col>
  </v-row>
  </div>

</template>

<style>
.main-header{
height: 20%;
border-bottom-left-radius: 2% ;
border-bottom-right-radius: 2% ;
padding: 70px 7%;
}
.main-col1{
display: flex;
flex-direction: column;
gap: 20;
}
.main-col2{
display: flex;
flex-direction: column;
gap: 30px;
}
.main-col2 v-btn.main-btn{
  font-size: 16px;
  font-weight: 600;
}
@media (max-width: 600px) {
  .main-header{
    padding: 50px 10%;
  }
}
</style>