<template>
    <div class="specs">
      <h2>Specifications</h2>
      <v-card v-for="spec in specifications" :key="spec.setup" class="spec-card" href="/bhk" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.secondary2}">
        <v-row no-gutters class="spec-row">
          <v-col cols="12" sm="2">
            <div class="image-wrapper">
              <v-img :src="spec.image" height="100%"></v-img>
            </div>
          </v-col>
          <v-col cols="12" sm="1">
            <v-divider vertical></v-divider>
          </v-col>
          <v-col cols="6" sm="2" class="specs-content">
            <div class="spec-label">Area</div>
            <div class="spec-value">{{ spec.area }}</div>
          </v-col>
          <v-col cols="6" sm="2" class="specs-content">
            <div class="spec-label">Setup</div>
            <div class="spec-value">{{ spec.setup }}</div>
          </v-col>
          <v-col cols="6" sm="2" class="specs-content">
            <div class="spec-label">Number of washrooms</div>
            <div class="spec-value">{{ spec.washrooms }}</div>
          </v-col>
          <v-col cols="6" sm="2" class="specs-content">
            <div class="spec-label">Apartments available</div>
            <div class="spec-value">{{ spec.apartments }}</div>
          </v-col>
        </v-row>
      </v-card>
    </div>
  </template>
  
  <script>
  export default {
    data: () => ({
      specifications: [
        {
          image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          area: '2500 sqft',
          setup: '3 BHK',
          washrooms: '2',
          apartments: '20'
        },
        {
          image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          area: '2500 sqft',
          setup: '2 BHK',
          washrooms: '2',
          apartments: '20'
        },
        {
          image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          area: '2500 sqft',
          setup: '1 BHK',
          washrooms: '2',
          apartments: '20'
        },
        {
          image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          area: '2500 sqft',
          setup: '5 BHK',
          washrooms: '2',
          apartments: '20'
        }
      ]
    })
  }
  </script>
  
  <style scoped>
  .specs {
    margin-top: 50px;
    padding: 0px 6%;
  }
  
  .specs h2 {
    text-align: left;
    font-size: 32px;
    font-weight: 700;
    margin-bottom: 50px;
  }
  .spec-card {
    display:flex;
    flex-direction: row;
    align-items:center;
    justify-content:center;
    flex-wrap: wrap;
    border-radius:20px;
    margin-bottom:15px;
  }
  .image-wrapper{
      height:auto;
      width:auto;
      margin-left:auto;
      margin-right:auto;
      border-radius:20px;
  }
  .specs-content{
      text-align:center;
  }
  .spec-label{
    font-weight: 400;
    font-size:12px;
  }
  .spec-value{
    font-weight: 700;
    font-size:24px;
  }
  @media (min-width:600px){
      .image-wrapper{
        height:auto;
        width:auto;
        margin-left:auto;
        margin-right:auto;
        border-radius:20px;  
      }
  }
  </style>
  