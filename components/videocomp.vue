<template>
<div class="video" id="project">
      <iframe
      width="87%" height="490" style="border:0; border-radius:21px"
   :src="videoSource"
   frameborder="0"
   allowfullscreen
 ></iframe>
</div>

</template>

<script>
export default {
  data() {
    return {
      videoSource: "https://www.youtube.com/embed/8IOevdLslhc" 
    };
  }
};
</script>

<style scoped>
.video{
  position: relative;
  display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 5%;
    padding-bottom: 3%;
}
</style>