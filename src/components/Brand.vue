<template>
  <div>
    <hooper :settings="hooperSettings">
      <slide v-for="(brand, i) in brandList" :key="i">
        <img :src="brand.src" alt="brand" />
      </slide>
    </hooper>
  </div>
</template>

<script>
import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";
export default {
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      brandList: [
        {
          src: require("../assets/img/_/brands/1200px-Fraunhofer-Gesellschaft_2009_logo.svg.png"),
        },
        {
          src: require("../assets/img/_/brands/226e28de7d1b42057e19dd7aa34a4bc2.png"),
        },
        {
          src: require("../assets/img/_/brands/Audi-Logo-PNG-Clipart-Background.gif"),
        },
        {
          src: require("../assets/img/_/brands/Lufthansa_Logo_2018.svg.png"),
        },
     
       
      ],
      hooperSettings: {
        infiniteScroll: true,
        wheelControl: false,
        autoPlay: false,
        mouseDrag: false,
        transition: 200,
        playSpeed: 1500,
        breakpoints: {
          1200: {
            itemsToShow: 4,
          },
          576: {
            itemsToShow: 3,
          },
          280: {
            itemsToShow: 2,
          },
        },
      },
    };
  },
};
</script>

<style lang="scss">
.hooper {
  height: auto;
}
</style>
