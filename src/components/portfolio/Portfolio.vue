<template>
  <div class="container">
    <div class="positon-relative">
      <div class="shane_tm_title">
        <div class="title_flex">
          <div class="left">
            <span>Portfolio</span>
            <h3>Creative Portfolio</h3>
          </div>
        </div>
      </div>
      <!-- End shane_tm_title -->
      <div class="portfolio_filter">
        <ul>
          <li>
            <a
              v-on:click="activetab = 1"
              :class="[activetab === 1 ? 'active' : '']"
              >All</a
            >
          </li>
          <!-- End All for tabcontent 1 -->
          <li>
            <a
              v-on:click="activetab = 2"
              :class="[activetab === 2 ? 'active' : '']"
              >Vimeo</a
            >
          </li>
          <!-- End Vimeo tabcontent 2 -->
          <li>
            <a
              v-on:click="activetab = 3"
              :class="[activetab === 3 ? 'active' : '']"
              >Youtube</a
            >
          </li>
          <!-- End .Youtube tabcontent 3 -->
          <li>
            <a
              v-on:click="activetab = 4"
              :class="[activetab === 4 ? 'active' : '']"
              >Gallery</a
            >
          </li>
          <!-- End Mix tabcontent 4 -->
        </ul>
      </div>
      <!-- End .portfolio-filter -->
    </div>

    <div v-if="activetab === 1" class="tabcontent">
      <div class="portfolio_list">
        <ul class="gallery_zoom">
          <CoolLightBox :items="allItems" :index="index" @close="index = null">
          </CoolLightBox>
          <li v-for="(image, imageIndex) in allItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry shane_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
      </div>

      <!-- End .portfolio_list -->
    </div>
    <!-- End .tabcontent 1 -->

    <div v-if="activetab === 2" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="vimeoItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>
          <li v-for="(image, imageIndex) in vimeoItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 2 -->

    <div v-if="activetab === 3" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="youtubeItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>
          <li v-for="(image, imageIndex) in youtubeItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 3 -->

    <div v-if="activetab === 4" class="tabcontent">
      <div class="portfolio_list">
        <ul>
          <CoolLightBox
            :items="galleryItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>

          <li v-for="(image, imageIndex) in galleryItems" :key="imageIndex">
            <div class="inner" @click="index = imageIndex">
              <div class="entry tokyo_tm_portfolio_animation_wrap">
                <img class="image" :src="image.thumb" alt="Portfolio" />
              </div>
              <!-- End .entry -->
              <div class="mobile_title">
                <h3>{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End .tabcontent 4 -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      activetab: 1,
      allItems: [
        {
          src: "https://vimeo.com/43338103",
          thumb: require("../../assets/img/portfolio/1.jpg"),
          portfolioName: "My Song",
          portfolioType: "AR/VR",
        },
        {
          src: require("../../assets/img/portfolio/2.jpg"),
          thumb: require("../../assets/img/portfolio/2.jpg"),
          portfolioName: "Fashion Memory",
          portfolioType: "UX",
        },
        {
          src: require("../..//assets/img/portfolio/14.jpg"),
          thumb: require("../../assets/img/portfolio/14.jpg"),
          portfolioName: "Childhood Memory",
          portfolioType: "3D",
        },
      ],
      vimeoItems: [
        {
          src: "https://vimeo.com/43338103",
          thumb: require("../../assets/img/portfolio/7.jpg"),
          portfolioName: "My Sound",
          portfolioType: "Vimeo",
        },
      ],
      youtubeItems: [
        {
          src: "https://youtu.be/YlBTaj0cXQY",
          thumb: require("../../assets/img/portfolio/7.jpg"),
          portfolioName: "Behance Design",
          portfolioType: "Youtube",
        },
      ],
      mixItems: [
        {
          src: require("../../assets/img/portfolio/2.jpg"),
          thumb: require("../../assets/img/portfolio/2.jpg"),
        },
        {
          src: "https://youtu.be/ZOoVOfieAF8",
          thumb: require("../../assets/img/portfolio/14.jpg"),
        },
      ],
      galleryItems: [
        {
          src: require("../../assets/img/portfolio/3.jpg"),
          thumb: require("../../assets/img/portfolio/3.jpg"),
          portfolioName: "Beautiful Memory",
          portfolioType: "Gallery",
        },
      ],
      index: null,
    };
  },
};
</script>

<style lang="scss" scoped></style>
