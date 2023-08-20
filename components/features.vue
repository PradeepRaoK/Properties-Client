<template>
    <div class="container" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.secondary2}">
        <v-container>
            <v-row class="header">
                    <h2>Features and Amenities</h2>
            </v-row>
            <v-row class="items">
              <v-col v-for="item in features" :key="item.name" cols="6" sm="3" class="items-container">
                  <img src="images/carbon_circle-dash.svg" alt="feature"/>
                  <p> {{item.name}}</p>
              </v-col>
            </v-row>
          </v-container>
    </div>
  </template>
  
  <script>
 
  export default {
    data: () => ({
      features:[
        {
            name:'Amenity one'
        },
        {
            name:'Amenity two'
        },
        {
            name:'Amenity three'
        },
        {
            name:'Amenity four'
        },
        {
            name:'Amenity five'
        },
        {
            name:'Amenity six'
        },
        {
            name:'Amenity seven'
        },
        {
            name:'Amenity eight'
        }
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
  