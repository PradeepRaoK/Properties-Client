<template>
    <div class="container" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.secondary2}">
        <v-container>
            <v-row class="header">
                    <h2>Nearby Places</h2>
            </v-row>
            <v-row class="items">
              <v-col v-for="item in places" :key="item.name" cols="6" sm="3" class="items-container">
                  <img src="images/carbon_circle-dash.svg" alt="feature"/>
                  <h3>{{item.distance}}</h3>
                  <p> {{item.name}}</p>
              </v-col>
            </v-row>
          </v-container>
    </div>
  </template>
  
  <script>
 
  export default {
    data: () => ({
      places:[
        {
            distance:'3 kms away',
            name:'Hospital'
        },
        {
            distance:'500m away',
            name:'Park'
        },
        {
            distance:'1 km away',
            name:'School'
        },
        {
            distance:'5 kms away',
            name:'Airport'
        },
        {
            distance:'3 kms away',
            name:'Hospital'
        },
        {
            distance:'500m away',
            name:'Park'
        },
        {
            distance:'1 km away',
            name:'School'
        },
        {
            distance:'5 kms away',
            name:'Airport'
        },
      ]
    }),
  }
  </script>
  
  <style scoped>
  .container{
    height: 488px;
    display: flex;
    justify-content: center;
    align-items: space-between;
    padding: 15px;
    margin-top: 20px;
    border-radius: 21px;
    margin-bottom: 20px;
  }
  .items {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px 0;
  }
  
  .header{
    margin-bottom: 80px;
  }

  .items-container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  </style>
  