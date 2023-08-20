<template>
    <div class="testimonials">
        <div class="container">
            <h2 class="header" :style="{color: $vuetify.theme.themes.myTheme.colors.primary2}">Testimonials</h2>
            <div class="arrows" :style="{color: $vuetify.theme.themes.myTheme.colors.primary2}">
                <v-icon @click="scrollImages(-1)">mdi-chevron-left</v-icon>
                <v-icon @click="scrollImages(1)">mdi-chevron-right</v-icon>
            </div>
        </div>
        <div class="images">
            <div class="image-container" v-for="item in testimonials" :key="item.title">
                <v-card class="mx-auto custom-card" max-width="344" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.secondary2}">
                    <div class="image-wrapper">
                        <v-row class="profile">
                            <v-avatar size="50" :image="item.image">
                            </v-avatar>
                            <v-col>
                                <v-row class="name">{{ item.name }}</v-row>
                                <v-row class="designation">{{ item.company }}</v-row>
                            </v-col>
                        </v-row>
                    </div>
                    <v-text class="text">
                        {{ item.testimonial }}
                    </v-text>
                </v-card>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data: () => ({
      testimonials:[
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            name:'Name 1',
            company: 'Company 1',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            name:'Name 2',
            company: 'Company 2',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            name:'Name 3',
            company: 'Company 3',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            name:'Name 4',
            company: 'Company 4',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            name:'Name 5',
            company: 'Company 5',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            name:'Name 6',
            company: 'Company 6',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            name:'Name 7',
            company: 'Company 7',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
            name:'Name 8',
            company: 'Company 8',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
            name:'Name 9',
            company: 'Company 9',   
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
        },
        {
            image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
            name:'Name 10',
            company: 'Company 10',
            testimonial: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo.',
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
.testimonials{
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
    border-radius: 10px;
    padding: 5px;
    margin: 10px;
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
.profile{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin: 5 auto;
    width: 100%;
    height: 100%;
}
.name{
    font-weight: 600;
    font-size: 24px;
}
.designation{
    font-weight: 400;
    font-size: 12px;
}
.text{
    font-size: 18px;
    font-weight: 400;
}
</style>