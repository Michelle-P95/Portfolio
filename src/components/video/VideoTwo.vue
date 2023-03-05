<template>
  <div class="shane_tm_section">
    <CoolLightBox :items="youtubeItems" :index="index" @close="index = null">
    </CoolLightBox>
    <div
      class="shane_tm_business_video"
      v-for="(image, imageIndex) in youtubeItems"
      :key="imageIndex"
    >
      <div class="bg">
        <div
          class="image jarallax"
          :style="{ backgroundImage: 'url(' + image.thumb + ')' }"
        ></div>
        <div class="overlay"></div>
      </div>
      <!-- End .bg -->

      <div class="content">
        <span
          class="rounded"
          @click="index = imageIndex"
          v-scroll-reveal="{ delay: 50, distance: '50px', duration: 1000 }"
        ></span>

        <h3
          class="text"
          v-scroll-reveal="{ delay: 100, distance: '50px', duration: 1200 }"
        >
          I am delivering beautiful digital products for my clients
        </h3>

        <div
          class="shane_tm_video_button"
          v-scroll-reveal="{ delay: 150, distance: '50px', duration: 1400 }"
        >
          <button class="popup-youtube" @click="index = imageIndex">
            Watch Video
          </button>
        </div>
      </div>
      <!-- End .content -->
    </div>
    <!-- End .shane_tm_business_video -->
  </div>
  <!-- End .shane_tm_section -->
</template>

<script>
export default {
  data() {
    return {
      index: null,
      youtubeItems: [
        {
          src: "https://youtu.be/ZOoVOfieAF8",
          thumb: require("../../assets/img/video/1.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
