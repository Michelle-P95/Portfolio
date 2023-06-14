<template>
  <div class="slider-four">
    <div class="shane_tm_hero" id="home" data-style="one">
      <vue-particles
        color="#dedede"
        :particleOpacity="0.7"
        :particlesNumber="22"
        shapeType="circle"
        :particleSize="6"
        linesColor="#dedede"
        :linesWidth="0"
        :lineLinked="true"
        :lineOpacity="0"
        :linesDistance="0"
        :moveSpeed="5"
        :hoverEffect="true"
        hoverMode="repulse"
        :clickEffect="false"
        clickMode="push"
      >
      </vue-particles>
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
            <h3 style="text-decoration: none; font-size: 75px; ">
              <span
                >Michelle <br />
                Poetsch</span>
              <br />

              <span class="typed-text loop-text">{{ typeValue }}</span>
              <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
              <span class="overlay_effect"></span>
            </h3>
          </div>
          <!-- End title -->

          <div class="job_wrap">
            <span class="job" style="font-size: 20px">
              based in Europe.
              <span class="overlay_effect"></span>
            </span>
          </div>
          <!-- End designation -->

          <a href="#portfolio" class="white-fill-bg btn-outline btn-medium">
            SEE PORTFOLIO
            <span class="overlay_effect"></span>
          </a>
        </div>
        <!-- End content -->
      </div>
      <!-- End .container -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sliderHero: require("../../assets/img/_/pflanzen.jpg"),
      typeValue: "",
      typeStatus: false,
      typeArray: ["Designer | Developer.", "UX Designer.", "AR/XR Designer.", "APP Developer.", "Frontend Developer.", "Product Designer.", "3D/CAD Designer."],
      typingSpeed: 130,
      erasingSpeed: 100,
      newTextDelay: 1100,
      typeArrayIndex: 0,
      charIndex: 0,
    };
  },
  methods: {
    typeText() {
      if (this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true;

        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;

        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;

        this.typeValue = this.typeArray[this.typeArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.typeArrayIndex += 1;
        if (this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0;

        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },
};
</script>

<style lang="scss" scoped>
.cursor {
  display: inline-block;
  margin-left: 3px;
  width: 4px;
  background-color: #fff;
  animation: cursorBlink 1s infinite;
}

span.cursor.typing {
  animation: none;
}

@keyframes cursorBlink {
  49% {
    background-color: #fff;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}
#particles-js {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 5;
  @media screen and (max-width: 767px) {
    display: none;
  }
}
</style>
