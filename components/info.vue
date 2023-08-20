<template>
    <div class="container">
        <div>
            <v-table>
                <tbody>
                  <tr
                    v-for="item in items"
                    :key="item.name"
                  >
                    <td class="table-left">{{ item.name }}</td>
                    <td>{{ item.value }}</td>
                  </tr>
                </tbody>
              </v-table>
        </div>
        <div class="bnk">
            <p class="table-left" :style="{color:$vuetify.theme.themes.myTheme.colors.quaternary2}">Approved Banks</p>
            <v-divider></v-divider>
            <div class="banks-container">
                <div v-for="bank in banks" :key="bank.img">
                    <v-card :text="bank.img" variant="tonal"></v-card>
                  </div>                  
              </div>              
        </div>
    </div>
  </template>
  <script>
  export default {
    data () {
      return {
        items: [
          {
            name: 'Location',
            value: 'Bejai, Mangalore',
          },
          {
            name: 'Project status',
            value: 'Upcoming',
          },
          {
            name: 'Project type',
            value: 'Residential',
          },
          {
            name: 'Builders',
            value: 'Someshwar builders',
          },
        ],
        banks:[
            {
                img: 'Bank Logos'
            },
            {
                img: 'Bank Logos'
            }
        ]
      }
    },
  }
</script>

<style scoped>
*{
    font-family: 'Lato', sans-serif;
    margin: 25px;
    box-sizing: border-box;
}
td {
border-bottom: 0.5px solid rgb(182, 182, 182);
}
.table-left{
    font-weight: 400;
    font-size: 16px;
}
.banks-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    margin-top: 20px;
    gap: 20px;
  }  
.container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .container > div {
    width: 50%;
  }
  .bnk{
    margin: 20px;
  }
  @media (max-width: 600px) {
    .container {
      flex-direction: column;
    }
    .container > div {
      width: 100%;
    }
  }
</style>