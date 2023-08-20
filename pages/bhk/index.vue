<template>
    <Navbar/>
    <div class="head">
        <h1>2BHK</h1>
        <p>Someshwar Vista, Mangalore</p>
    </div>
    <Carousel/>
    <About/>
    <Features/>
    <Floorplan/>
    <Brochure/>
    <Footer/>
</template>
<script>
export default {
    data() {
        return {
            bhk: true,
        }
    },
}
</script>

<style scoped>
.head{
    margin-left: 85px;
}
</style>