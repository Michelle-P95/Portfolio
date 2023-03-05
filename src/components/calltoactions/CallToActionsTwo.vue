<template>
  <div
    class="shane_tm_talk bg_image_props"
    :style="{ backgroundImage: 'url(' + imgSrc + ')' }"
    id="contact"
  >
    <div class="shape">
      <img
        class="svg"
        src="../../assets/img/svg/paper.svg"
        alt="partners brand"
      />
    </div>
    <!-- End shape -->

    <div class="background" id="talk">
      <a class="player"></a>
      <div class="overlay"></div>
    </div>
    <!-- End background -->

    <div class="talk_inner">
      <div class="text" v-scroll-reveal="{ delay: 100 }">
        <h3>Let's work together!</h3>
      </div>
      <div class="button" v-scroll-reveal="{ delay: 200 }">
        <button class="white-fill-bg" @click="showModal">
          Make an enquiry
        </button>
      </div>
    </div>
    <!-- End talk_inner -->

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
          <div class="modal-content calltoactions-content">
            <div class="close" @click="closeModal">
              <img
                class="svg"
                src="../../assets/img/svg/cancel.svg"
                alt="cancel-img"
              />
            </div>
            <!-- End .close -->

            <div class="shane_tm_mobalbox_contact">
              <div class="box_inner">
                <div class="title">
                  <h3>Get in Touch</h3>
                </div>

                <div class="wrapper">
                  <div class="left">
                    <div class="fields">
                      <Contact />
                    </div>
                  </div>
                  <!-- End left -->
                  <div class="right">
                    <div class="map_wrap">
                      <Map />
                    </div>
                  </div>
                  <!-- End right -->
                </div>
                <!-- End wrapper -->

                <div class="short_info">
                  <ul>
                    <li>
                      <div class="list_inner">
                        <img
                          class="svg"
                          src="../../assets/img/svg/location.svg"
                          alt="location"
                        />
                        <p>Brook 103, 90021 New York, USA</p>
                      </div>
                    </li>
                    <!-- End silgle address -->

                    <li>
                      <div class="list_inner">
                        <img
                          class="svg"
                          src="../../assets/img/svg/phone.svg"
                          alt="phone"
                        />
                        <p>
                          <a href="tel:+77 033 442 55 57">+77 033 442 55 57</a>
                        </p>
                      </div>
                    </li>
                    <!-- End silgle address -->

                    <li>
                      <div class="list_inner">
                        <img
                          class="svg"
                          src="../../assets/img/svg/share.svg"
                          alt="share"
                        />

                        <Social />
                      </div>
                    </li>
                    <!-- End silgle address -->
                  </ul>
                </div>
                <!-- End modal conetent -->
              </div>
              <!-- End box inner -->
            </div>
            <!-- End modalbox news -->
          </div>
        </div>
      </div>
    </transition>
    <!-- End Modalbox -->
  </div>
  <!-- Start Modal -->
</template>

<script>
import Contact from "../Contact.vue";
import Map from "../Map.vue";
import Social from "../Social.vue";
export default {
  components: {
    Contact,
    Map,
    Social,
  },
  data() {
    return {
      imgSrc: require("../../assets/img/callto-action/2.jpg"),
      isActive: false,
      isVisible: false,
    };
  },
  methods: {
    showModal: function() {
      this.isActive = true;
      this.isVisible = true;
    },
    closeModal: function() {
      this.isActive = false;
      this.isVisible = false;
    },
  },
};
</script>

<style lang="scss" scoped></style>
