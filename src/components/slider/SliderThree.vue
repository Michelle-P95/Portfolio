<template>
  <div class="slider-three">
    <div class="shane_tm_hero" id="home" data-style="two">
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
            <h3><span>Robert</span> Hr.<span class="overlay_effect"></span></h3>
          </div>
          <!-- End title -->

          <div class="job_wrap">
            <span class="job">
              Sr. Software Engineer
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
  </div>
</template>

<script>
export default {
  data() {
    return {
      sliderHero: require("../../assets/img/slider/1.jpg"),
    };
  },
};
</script>

<style lang="scss"></style>
