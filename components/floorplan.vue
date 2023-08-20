<template>
    <div class="gallery">
        <div class="container">
            <h2 class="header" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">Floorplans</h2>
        </div>
        <div class="images">
            <div class="image-container" v-for="item in gallery" :key="item.title">
                <v-card class="mx-auto custom-card" max-width="300">
                    <div class="image-wrapper">
                        <v-img
                        :src="item.image"
                        height="320px"
                        radius="21px"
                        cover
                    ></v-img>
                    </div>

                    <v-card-title>
                        {{ item.title }}
                    </v-card-title>
                </v-card>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data: () => ({
      gallery:[
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Floorplan 1',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Floorplan 2',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Floorplan 3',
        },
      ],
      currentImageIndex: 0,
    }),
    methods: {
        scrollImages(direction) {
        const imagesElement = this.$el.querySelector('.images');
        const scrollAmount = direction * 360; // Adjust this value to control the amount of scrolling
        imagesElement.scrollBy({ left: scrollAmount, behavior: 'smooth' });
  }
}

  }
</script>
<style scoped>
*{
    font-family: 'Lato', sans-serif;
    margin: 5px;
}
.gallery{
    padding: 0 4%;
}
.container{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin: 5 auto;
    width: 100%;
    height: 100%;
}
.header{
    font-weight: 700;
    font-size: 32px;
    margin-left: 25px;
}
.images {
    display: flex;
    overflow-x: scroll; /* Enable horizontal scrolling */
    scrollbar-width: thin;
    scrollbar-color: #999 transparent;
}
.images::-webkit-scrollbar {
    height: 8px;
}
.images::-webkit-scrollbar-thumb {
    background-color: #999;
    border-radius: 4px;
}
.image-container {
    flex: 0 0 344px; /* Set a fixed width for each image container */
    margin-right: 16px;
}
.images::after {
    content: ''; /* Create a pseudo-element to fill remaining space */
    flex: 0 0 16px; /* Adjust for margin-right of the last item */
}
.image-wrapper{
    border-radius: 21px;
}
.custom-card {
    border: none !important; /* Remove border around v-card */
    box-shadow: none !important; /* Remove box shadow if any */
}

</style>