<template>
  <div>
    <div class="shane_tm_all_wrap">
      <div class="shane_tm_intro">
        <div
          class="hero"
          :style="{ backgroundImage: 'url(' + heroIntro + ')' }"
        >
          <div class="content">
            <img
              src="../assets/img/logo/new/logo.png"
              class="prev-logo"
              alt="logo"
              v-scroll-reveal="{ delay: 150 }"
            />
            <p v-scroll-reveal="{ delay: 100 }">
              VueJS Personal Portfolio Template
            </p>
            <div v-scroll-reveal="{ delay: 200 }">
              <a href="#demos" class="white-fill-bg btn-outline btn-medium">
                SEE ALL DEMO
              </a>
            </div>

            <!-- End purchase_button -->
          </div>
        </div>
        <!-- End .hero -->

        <div class="demo_list" id="demos">
          <div class="container">
            <div class="intro_title">
              <h3>All Ready Demos</h3>
            </div>
            <div class="inner">
              <ul>
                <li v-scroll-reveal="{ delay: 50 }">
                  <div class="list_inner">
                    <img src="../assets/img/intro/1.jpg" alt="demo preview" />
                    <h3>Main Demo (No Animation)</h3>
                    <router-link
                      to="/main-demo"
                      class="shane_tm_full_link"
                      target="_blank"
                    ></router-link>
                  </div>
                </li>
                <!-- End list_inner -->

                <li v-scroll-reveal="{ delay: 100 }">
                  <div class="list_inner">
                    <img src="../assets/img/intro/2.jpg" alt="demo preview" />
                    <h3>Creative Portfolio</h3>
                    <router-link
                      to="/creative-portfolio"
                      class="shane_tm_full_link"
                      target="_blank"
                    ></router-link>
                  </div>
                </li>
                <!-- End list_inner -->

                <li v-scroll-reveal="{ delay: 150 }">
                  <div class="list_inner">
                    <img src="../assets/img/intro/3.jpg" alt="demo preview" />
                    <h3>Modern Portfolio</h3>
                    <router-link
                      to="/modern-portfolio"
                      class="shane_tm_full_link"
                      target="_blank"
                    ></router-link>
                  </div>
                </li>
                <!-- End list_inner -->

                <li v-scroll-reveal="{ delay: 200 }">
                  <div class="list_inner">
                    <img src="../assets/img/intro/4.jpg" alt="demo preview" />
                    <h3>Creative Portfolio 02</h3>
                    <router-link
                      to="/creative-portfolio-02"
                      class="shane_tm_full_link"
                      target="_blank"
                    ></router-link>
                  </div>
                </li>
                <!-- End list_inner -->
              </ul>
            </div>
          </div>
        </div>

        <div class="shane_tm_feature section-separaton">
          <div
            class="intro_title"
            v-scroll-reveal="{ delay: 250, distance: '20px' }"
          >
            <h3>Shane All Features</h3>
          </div>
          <!-- End .intro_title -->
          <div class="container fluid">
            <div class="row">
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 200, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/1.svg" alt="icon" />
                  <h4>Latest React 17.0.2</h4>
                  <p>
                    We used latest react vertion ^17.0.2. Its a awesome design
                    made by react.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 300, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/2.svg" alt="icon" />
                  <h4>No Bootstrap!</h4>
                  <p>
                    Made this template no framework dependency.Usage 100% hand
                    made pure CSS.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 400, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/3.svg" alt="icon" />
                  <h4>Perfect Responsive</h4>
                  <p>
                    Shane is fit for all devices like mobile,tablet,desktop even
                    larger device too.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 500, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/4.svg" alt="icon" />
                  <h4>Well Documented</h4>
                  <p>
                    Shane documented organized way and its customization
                    instruction easy for all.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 600, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/5.svg" alt="icon" />
                  <h4>Sass Available</h4>
                  <p>
                    Shane tamplate has Sass available for css. You can Change
                    css by sass
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 700, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/6.svg" alt="icon" />
                  <h4>Fast Loading Speed</h4>
                  <p>
                    Shane is faster loading speed.It's create your template so
                    much faster.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 800, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/7.svg" alt="icon" />
                  <h4>Modern Design</h4>
                  <p>
                    It's followed with modern, creative and trendy design for
                    Creative Organization.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
              <div
                class="col-3"
                v-scroll-reveal="{ delay: 900, distance: '20px' }"
              >
                <div class="single-features">
                  <img src="../assets/img/svg/preview/8.svg" alt="icon" />
                  <h4>24 Support System</h4>
                  <p>
                    We are provide 24 hours support for all clients.You can
                    purchase without hesitation.
                  </p>
                </div>
              </div>
              <!-- End .single-features -->
            </div>
          </div>
        </div>
      </div>
      <!-- End shame_tm_intro -->

      <div class="shane_tm_section">
        <div
          class="shane_purchase_banner"
          :style="{ backgroundImage: 'url(' + footerPattern + ')' }"
        >
          <div class="container">
            <h2 v-scroll-reveal="{ delay: 50 }">Let's go to Purchase</h2>
            <div class="shane_tm_button" v-scroll-reveal="{ delay: 150 }">
              <a href="#" target="_blank">
                PURCHASE NOW
              </a>
            </div>
          </div>
        </div>
      </div>

      <div class="shane_tm_section">
        <div class="shane_tm_copyright">
          <div class="container">
            <div class="inner">
              <p v-scroll-reveal="{ delay: 150, distance: '20px' }">
                &copy; {{ new Date().getFullYear() }} Shane
                <a
                  href="https://themeforest.net/user/ib-themes"
                  target="_blank"
                >
                  ib-themes
                </a>
                . All rights reserved.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroIntro: require("../../src/assets/img/video/1.jpg"),
      footerPattern: require("../../src/assets/img/patterns/1.png"),
    };
  },
};
</script>

<style lang="scss" scoped></style>
