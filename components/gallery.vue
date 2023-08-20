<template>
    <div class="gallery" id="gallery">
        <div class="container">
            <h2 class="header" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">Gallery</h2>
            <div class="arrows" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">
                <v-icon @click="scrollImages(-1)">mdi-chevron-left</v-icon>
                <v-icon @click="scrollImages(1)">mdi-chevron-right</v-icon>
            </div>
        </div>
        <div class="images">
            <div class="image-container" v-for="item in gallery" :key="item.title">
                <v-card class="mx-auto custom-card" max-width="344">
                    <div class="image-wrapper">
                        <v-img
                        :src="item.image"
                        height="200px"
                        radius="21px"
                        cover
                    ></v-img>
                    </div>

                    <v-card-title>
                        {{ item.title }}
                    </v-card-title>
                    <v-card-subtitle>
                        {{ item.subtitle }}
                    </v-card-subtitle>
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
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            subtitle: '1,000 miles of wonder'
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

.arrows {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    margin-top: -10px;
    margin-right: 15px;
    font-size: 24px;
}

.arrows v-icon {
    cursor: pointer;
    margin: 0 5px;
}
.gallery{
    padding: 0px 5%;
}
</style>