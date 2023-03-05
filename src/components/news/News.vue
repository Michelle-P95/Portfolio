<template>
  <div class="news_list">
    <ul>
      <li>
        <div class="list_inner">
          <div class="image">
            <img src="../../assets/img/placeholders/4-3.jpg" alt="thumb" />
            <div
              class="main"
              @click="showModal"
              :style="{ backgroundImage: 'url(' + imgSrc + ')' }"
            ></div>
          </div>
          <!-- End image -->

          <div class="details">
            <h3 class="title" @click="showModal">
              Developers watch out for these burnout symptoms
            </h3>
            <p class="date">
              By <a href="#">Alex Watson</a> <span>20 May 2020</span>
            </p>
          </div>
          <!-- End details -->
        </div>

        <!-- Start Modalbox -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive }"
            id="modal"
            @click="closeModal"
            v-if="isVisible"
          >
            <div class="modal-dialog modal-dialog-centered " @click.stop>
              <div class="modal-content">
                <div class="close" @click="closeModal">
                  <img
                    class="svg"
                    src="../../assets/img/svg/cancel.svg"
                    alt="cancel-img"
                  />
                </div>
                <!-- End .close -->

                <div class="shane_tm_modalbox_news">
                  <div class="box_inner">
                    <div class="image">
                      <img
                        src="../../assets/img/placeholders/4-3.jpg"
                        alt="thumb"
                      />
                      <div
                        class="main"
                        :style="{ backgroundImage: 'url(' + imgSrc + ')' }"
                      ></div>
                    </div>
                    <!-- End image -->
                    <div class="details">
                      <h3 class="title">
                        Developers watch out for these burnout symptoms
                      </h3>
                      <p class="date">
                        By <a href="#"> ALEX WATSON</a>
                        <span>20 May 2020</span>
                      </p>
                    </div>
                    <!-- End details -->

                    <div class="description">
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities. As Vintage decided to have a
                        closer look into fast-paced New York web design realm in
                        person, we get to acquaint with most diverse and
                        exceptionally captivating personalities.
                      </p>
                      <blockquote>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person. As Vintage decided
                        to have a closer look into fast-paced New York web
                        design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities.
                      </blockquote>
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. We encounter professionals with careers
                        to covet and lives to write books about. As Vintage
                        decided to have a closer look into fast-paced New York
                        web design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities.
                      </p>
                    </div>
                    <!-- End description -->

                    <div class="news_share">
                      <Social />
                    </div>
                    <!-- End news share -->
                  </div>
                  <!-- End .box_inner -->
                </div>
                <!-- shane_tm_modalbox_news -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End Modalbox -->
      </li>
      <!-- End li -->

      <li>
        <div class="list_inner">
          <div class="image">
            <img src="../../assets/img/placeholders/4-3.jpg" alt="thumb" />
            <div
              class="main"
              @click="showModal2"
              :style="{ backgroundImage: 'url(' + imgSrc2 + ')' }"
            ></div>
          </div>
          <!-- End image -->

          <div class="details">
            <h3 class="title" @click="showModal2">
              How to be appreciated for your hard work as a developer
            </h3>
            <p class="date">
              By <a href="#">BROOK KENNEDY </a> <span>07 Apr 2020</span>
            </p>
          </div>
          <!-- End details -->
        </div>

        <!-- Start Modalbox -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive2 }"
            id="modal"
            @click="closeModal2"
            v-if="isVisible2"
          >
            <div class="modal-dialog modal-dialog-centered " @click.stop>
              <div class="modal-content">
                <div class="close" @click="closeModal2">
                  <img
                    class="svg"
                    src="../../assets/img/svg/cancel.svg"
                    alt="cancel-img"
                  />
                </div>
                <!-- End .close -->
                <div class="shane_tm_modalbox_news">
                  <div class="box_inner">
                    <div class="image">
                      <img
                        src="../../assets/img/placeholders/4-3.jpg"
                        alt="thumb"
                      />
                      <div
                        class="main"
                        :style="{ backgroundImage: 'url(' + imgSrc2 + ')' }"
                      ></div>
                    </div>
                    <!-- End image -->
                    <div class="details">
                      <h3 class="title">
                        How to be appreciated for your hard work as a developer
                      </h3>
                      <p class="date">
                        By <a href="#">Brook Kennedy</a>
                        <span>07 April 2020</span>
                      </p>
                    </div>
                    <!-- End details -->

                    <div class="description">
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities. As Vintage decided to have a
                        closer look into fast-paced New York web design realm in
                        person, we get to acquaint with most diverse and
                        exceptionally captivating personalities.
                      </p>
                      <blockquote>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person. As Vintage decided
                        to have a closer look into fast-paced New York web
                        design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities.
                      </blockquote>
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. We encounter professionals with careers
                        to covet and lives to write books about. As Vintage
                        decided to have a closer look into fast-paced New York
                        web design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities.
                      </p>
                    </div>
                    <!-- End description -->

                    <div class="news_share">
                      <Social />
                    </div>
                    <!-- End news share -->
                  </div>
                  <!-- End .box_inner -->
                </div>
                <!-- shane_tm_modalbox_news -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End Modalbox -->
      </li>
      <!-- End li -->

      <li>
        <div class="list_inner">
          <div class="image">
            <img src="../../assets/img/placeholders/4-3.jpg" alt="thumb" />
            <div
              class="main"
              @click="showModal3"
              :style="{ backgroundImage: 'url(' + imgSrc3 + ')' }"
            ></div>
          </div>
          <!-- End image -->

          <div class="details">
            <h3 class="title" @click="showModal3">
              How designers and developers can collaborate better
            </h3>
            <p class="date">
              By <a href="#">PAOLA ATKINS</a> <span>02 March 2020</span>
            </p>
          </div>
          <!-- End details -->
        </div>

        <!-- Start Modalbox -->
        <transition name="fade">
          <!-- Modal -->
          <div
            :class="{ 'modal-mask': isActive3 }"
            id="modal"
            @click="closeModal3"
            v-if="isVisible3"
          >
            <div class="modal-dialog modal-dialog-centered " @click.stop>
              <div class="modal-content">
                <div class="close" @click="closeModal3">
                  <img
                    class="svg"
                    src="../../assets/img/svg/cancel.svg"
                    alt="cancel-img"
                  />
                </div>
                <!-- End .close -->
                <div class="shane_tm_modalbox_news">
                  <div class="box_inner">
                    <div class="image">
                      <img
                        src="../../assets/img/placeholders/4-3.jpg"
                        alt="thumb"
                      />
                      <div
                        class="main"
                        :style="{ backgroundImage: 'url(' + imgSrc3 + ')' }"
                      ></div>
                    </div>
                    <!-- End image -->
                    <div class="details">
                      <h3 class="title">
                        How designers and developers can collaborate better
                      </h3>
                      <p class="date">
                        By <a href="#"> PAOLA ATKINS</a>
                        <span>02 March 2020</span>
                      </p>
                    </div>
                    <!-- End details -->

                    <div class="description">
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities. As Vintage decided to have a
                        closer look into fast-paced New York web design realm in
                        person, we get to acquaint with most diverse and
                        exceptionally captivating personalities.
                      </p>
                      <blockquote>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person. As Vintage decided
                        to have a closer look into fast-paced New York web
                        design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities.
                      </blockquote>
                      <p>
                        As Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. We encounter professionals with careers
                        to covet and lives to write books about. As Vintage
                        decided to have a closer look into fast-paced New York
                        web design realm in person, we get to acquaint with most
                        diverse and exceptionally captivating personalities. As
                        Vintage decided to have a closer look into fast-paced
                        New York web design realm in person, we get to acquaint
                        with most diverse and exceptionally captivating
                        personalities. As Vintage decided to have a closer look
                        into fast-paced New York web design realm in person, we
                        get to acquaint with most diverse and exceptionally
                        captivating personalities.
                      </p>
                    </div>
                    <!-- End description -->

                    <div class="news_share">
                      <Social />
                    </div>
                    <!-- End news share -->
                  </div>
                  <!-- End .box_inner -->
                </div>
                <!-- shane_tm_modalbox_news -->
              </div>
            </div>
          </div>
        </transition>
        <!-- End Modalbox -->
      </li>
      <!-- End li -->
    </ul>
  </div>
</template>

<script>
import Social from "../Social.vue";
export default {
  components: {
    Social,
  },
  data() {
    return {
      isActive: false,
      isActive2: false,
      isActive3: false,
      isVisible: false,
      isVisible2: false,
      isVisible3: false,
      imgSrc: require("../../assets/img/news/1.jpg"),
      imgSrc2: require("../../assets/img/news/2.jpg"),
      imgSrc3: require("../../assets/img/news/3.jpg"),
    };
  },
  methods: {
    showModal: function() {
      this.isActive = true;
      this.isVisible = true;
    },
    showModal2: function() {
      this.isActive2 = true;
      this.isVisible2 = true;
    },
    showModal3: function() {
      this.isActive3 = true;
      this.isVisible3 = true;
    },
    closeModal: function() {
      this.isActive = false;
      this.isVisible = false;
    },
    closeModal2: function() {
      this.isActive2 = false;
      this.isVisible2 = false;
    },
    closeModal3: function() {
      this.isActive3 = false;
      this.isVisible3 = false;
    },
  },
};
</script>

<style lang="scss" scoped></style>
