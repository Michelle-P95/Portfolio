<template>
  <div class="shane_tm_hero" id="home" data-style="one">
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
          <h3><span>Ave</span> Brook<span class="overlay_effect"></span></h3>
        </div>
        <!-- End title -->

        <div class="job_wrap">
          <span class="job">
            Independent Web Developer
            <span class="overlay_effect"></span>
          </span>
        </div>
        <!-- End designation -->
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
</template>

<script>
export default {
  data() {
    return {
      sliderHero: require("../../assets/img/slider/4.jpg"),
    };
  },
};
</script>

<style lang="scss" scoped></style>
