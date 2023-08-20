<template>
  <div class="footer" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">
    <v-row > 
      <v-col  md="5" sm="12" cols="12"  align="center">
        <v-img
        width="80"
        height="80"
        cover
        src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
      ></v-img></v-col>
    <v-col  md="3" sm="12" cols="12" class="col-flex1">
      <v-text style="font-size: 32px;font-weight: 700;">Address</v-text>
      <v-text style="font-size: 16px;font-weight: 400;">Lorem ipsum dolor sit amet 
      consectetur tristique egestas hendrerit metus id ultrices vel justo hendrerit</v-text>
      <v-text style="font-size: 16px;font-weight: 400;">+91 1234567890</v-text>
    </v-col>
    <v-col  md="4" sm="12" cols="12" class="col-flex2">
    <v-text style="font-size: 32px;font-weight: 700;">Social Medias</v-text>
    <v-btn variant="plain" style="justify-content: left;font-size: 16px;font-weight: 400;">Instagram</v-btn>
    <v-btn variant="plain" style="justify-content: left;font-size: 16px;font-weight: 400;">Facebook</v-btn>
    <v-btn variant="plain" style="justify-content: left;font-size: 16px;font-weight: 400;">Linkedin</v-btn>
    <v-btn variant="plain" style="justify-content: left;font-size: 16px;font-weight: 400;">Threads</v-btn>
    </v-col>
    </v-row>
    <v-row class="copyright">
      <v-text style="font-size: 12px;font-weight: 400;">Copyright Exelon lorem ipsum</v-text>
    </v-row>
  
  </div>  
</template>

<style>
.footer{
  padding: 5%  7% 0 7%;
  height: 320px;
}
.col-flex1{
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.col-flex2{
  display: flex;
  flex-direction: column;
}
@media (max-width:960px) {
  .footer{
    height: 565px;
  }
  .copyright{
  margin-top:3% ;
  padding: 1% 0 1% 1%;
  border-top:0.2px solid #32270B;
  justify-content: center;
}
}

</style>