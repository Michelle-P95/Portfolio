<template>
  <div class="home-one">
    <Header />
    <!-- End Header Section -->

    <Slider />
    <!-- End Slider Section -->

    <div class="shane_tm_section" id="about">
      <div class="shane_tm_about">
        <div class="container">
          <About />
        </div>
        <!--  End container -->
      </div>
    </div>
    <!-- End About Section -->

    <div class="shane_tm_section" id="portfolio">
      <div class="shane_tm_portfolio">
        <Portfolio />
      </div>
    </div>
    <!-- End Portfolio Section -->

    <Skills />
    <!-- End Skills Section -->

    <Video />
    <!-- End Video Section -->

    <div class="shane_tm_section">
      <div class="shane_tm_partners">
        <div class="container">
          <div class="partners_inner">
            <Brand />
          </div>
        </div>
      </div>
    </div>
    <!-- End shane_tm_partners -->

    <div class="shane_tm_section">
      <div class="shane_tm_testimonials">
        <div class="container">
          <div class="testimonials_inner">
            <div class="left">
              <div class="shane_tm_title">
                <span>Testimonials</span>
                <h3>What clients say about my portfolio template</h3>
              </div>
            </div>

            <div class="right">
              <Testimonial />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End  shane_tm_testimonials -->

    <div class="shane_tm_section" id="news">
      <div class="shane_tm_news">
        <div class="container">
          <div class="shane_tm_title">
            <span>News</span>
            <h3>Latest News</h3>
          </div>
          <!-- End shane_tm_title -->
          <News />
          <!-- End news  -->
        </div>
      </div>
    </div>
    <!-- End  news -->

    <CallToActions />
    <!-- End  call to actions -->

    <Footer />
    <!-- End  footer  -->
  </div>
</template>

<script>
import Header from "../../components/Header";
import Slider from "../../components/slider/Slider";
import About from "../../components/about/About";
import Portfolio from "../../components/portfolio/Portfolio";
import Skills from "../../components/skills/Skills";
import Video from "../../components/video/Video";
import Brand from "../../components/Brand";
import Testimonial from "../../components/testimonial/Testimonial.vue";
import News from "../../components/news/News.vue";
import CallToActions from "../../components/calltoactions/CallToActions.vue";
import Footer from "../../components/Footer.vue";
export default {
  components: {
    Header,
    Slider,
    About,
    Portfolio,
    Skills,
    Video,
    Brand,
    Testimonial,
    News,
    CallToActions,
    Footer,
  },
};
</script>

<style lang="scss" scoped></style>
