<template>
  <div class="slider-two">
    <div class="shane_tm_hero" id="home" data-style="three">
      <div class="background">
        <div
          class="image"
          :style="{ backgroundImage: 'url(' + sliderHero + ')' }"
        ></div>
      </div>
      <!-- End .background -->

      <div class="container">
        <div class="content">
          <div class="name_wrap">
            <h3><span>Mrs</span> Iqra<span class="overlay_effect"></span></h3>
          </div>
          <!-- End title -->

          <div class="job_wrap">
            <span class="job">
              Ui & Ux Designer
              <span class="overlay_effect"></span>
            </span>
          </div>
          <!-- End designation -->
          <Social />
        </div>
        <!-- End content -->

        <div class="shane_tm_down loaded">
          <div class="line_wrapper">
            <div class="line"></div>
          </div>
        </div>
      </div>
      <!-- End .container -->
    </div>
  </div>
</template>

<script>
import Social from "../SocialTwo.vue";
export default {
  components: {
    Social,
  },
  data() {
    return {
      sliderHero: require("../../assets/img/slider/2.jpg"),
    };
  },
};
</script>

<style lang="scss" scoped></style>
