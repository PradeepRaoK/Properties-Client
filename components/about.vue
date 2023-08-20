<template>
    <div class="about" id="about" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}"> 
      <v-row>
        <v-col cols="12" md="6"> <v-text style="font-size: 32px;font-weight: 700;">About us</v-text></v-col>
        
    <v-col class="about-col" cols="12" md="6">
      <v-text style="font-size: 24px;font-weight: 400;">Lorem ipsum dolor sit amet consectetur. Morbi metus libero vulp
        utate habitant morbi diam in molestie.Consectetur risus natoque velit nullam curabitur et tincidunt.
        Lorem ipsum dolor sit amet consectetur. Morbi metus libero vulputate habitant morbi diam in molestie.Consectetur risus natoque. </v-text>
     
      </v-col>
      </v-row>   
     
  </div>
</template>
<style>
.about{
padding: 80px 7%;
}
.about-col{
  color: #6D6D6D;
}
</style>