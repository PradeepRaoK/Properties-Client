<template>
<div class="why-us" :style="{ backgroundColor: $vuetify.theme.themes.myTheme.colors.secondary2 }">
  <v-row>
    <v-col cols="12" md="6" align="center">
      <v-img
        width="250"
        height="380"
        cover
        style="border-radius: 5%;"
        src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
      ></v-img>
    </v-col>
    <v-col class="why-us-text" cols="12" md="6" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">
      <v-text style="font-size: 32px;font-weight: 700;">Why us?</v-text>
      <v-text style="font-size: 16px;font-weight: 400;">Lorem ipsum dolor sit amet consectetur. Morbi metus libero vulp
        utate habitant morbi diam in molestie.Consectetur risus natoque velit nullam curabitur et tincidunt. </v-text>
       
       <div class="divider"><v-img src="/images/thumbs.png" width="32" height="32" style="display: inline-block;margin-right: 20px;"></v-img><v-text style="font-size: 24px;font-weight: 700;">Main pointer goes here, short pointer</v-text></div>
      
       <div class="divider"><v-img src="/images/thumbs.png" width="32" height="32" style="display: inline-block;margin-right: 20px;"></v-img><v-text style="font-size: 24px;font-weight: 700;">Main pointer goes here, short pointer</v-text></div>
     
       <div class="divider3"><v-img src="/images/thumbs.png" width="32" height="32" style="display: inline-block;margin-right: 20px;"></v-img><v-text style="font-size: 24px;font-weight: 700;">Main pointer goes here, short pointer</v-text></div>
      
      </v-col>
  </v-row>
   
  </div>

</template>

<style>
.why-us{
  height: 25%;
  padding: 10% 7%;
}
.why-us-text{
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.divider{
  border-top:1px solid #6D6D6D;
  padding-top: 4%;
}
.divider3{
  border-top:1px solid #6D6D6D;
  border-bottom:1px solid #6D6D6D;
  padding-top: 4%;
  padding-bottom: 4%;
}

@media (max-width:960px)
{ 
  .why-us{
    text-align: center;
  }
  .why-us .img-col{
    text-align: center;
  }
}

</style>