<template>
    <div class="blogs" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.secondary2}">
        <div class="container">
            <h2 class="header" :style="{color:$vuetify.theme.themes.myTheme.colors.tertiary}">Blogs</h2>
            <div class="arrows" :style="{color:$vuetify.theme.themes.myTheme.colors.primary2}">
                <v-icon @click="scrollImages(-1)">mdi-chevron-left</v-icon>
                <v-icon @click="scrollImages(1)">mdi-chevron-right</v-icon>
            </div>
        </div>
        <div class="images">
            <div class="image-container" v-for="item in blogs" :key="item.title">
                <v-card class="mx-auto custom-card" color="secondary2" max-width="344">
                    <div class="image-wrapper">
                        <v-img
                        :src="item.image"
                        height="200px"
                        radius="21px"
                        cover
                    ></v-img>
                    </div>
                    <v-divider></v-divider>
                    <div class="author-details">
                        <v-text>{{item.author}}</v-text>
                        <v-text>{{item.date}}</v-text>
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
      blogs:[
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            title: 'Top western road trips',
            author: 'John Doe',
            date: '2020-01-01',
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
    margin: 20px auto;
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

.author-details{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-top: 10px;
    font-weight: 400;
    font-size: 12px;
}
.blogs{
    margin: 5px 0;
    padding: 0 5%;
}
v-card-title{
    font-weight: 600;
    font-size: 24px;
}

</style>