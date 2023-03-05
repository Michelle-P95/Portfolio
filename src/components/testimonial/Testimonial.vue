<template>
  <hooper :settings="hooperSettings">
    <slide v-for="(tesimonial, i) in testimonialContent" :key="i">
      <ul>
        <li class="item">
          <div class="texts">
            <p>
              {{ tesimonial.desc }}
            </p>
            <div class="author">
              <div class="image">
                <div
                  class="main"
                  :style="{ backgroundImage: 'url(' + tesimonial.imgSrc + ')' }"
                ></div>
              </div>
              <div class="short">
                <h3 class="author">
                  <span>{{ tesimonial.name }}</span>
                </h3>
                <h3 class="job">
                  <span>{{ tesimonial.designation }}</span>
                </h3>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </slide>
  </hooper>
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
      testimonialContent: [
        {
          name: "Justin Bieber",
          designation: "Photographer",
          imgSrc: require("../../assets/img/about/1.jpg"),
          desc: `We were looking for a logo with a touch of modernism. Arlo grasped our
          needs and produced a stunning design. Awesome to work with Arlo.
          Incredibly organized, easy to communicate with, responsive with next
          iterations.`,
        },
        {
          name: "Teodor Federico",
          designation: "Freelancer",
          imgSrc: require("../../assets/img/about/2.jpg"),
          desc: ` I purchased the theme a few weeks ago. I had some issues with the
              theme, I asked customer support to help me with and they were
              helpful and kind to help me with all my problems. I definitely
              recommend this theme to everyone.`,
        },
        {
          name: "Bauen Fernandes",
          designation: "Web Developer",
          imgSrc: require("../../assets/img/about/3.jpg"),
          desc: `Really the Code, Support, and design are awesome and its good
              support they are giving. They give an instant solution to our
              needs. Really awesome. I will strongly recommend to my friends.
              Great template, even better service!`,
        },
      ],
      hooperSettings: {
        infiniteScroll: true,
        wheelControl: false,
        autoPlay: true,
        mouseDrag: false,
        transition: 600,
        playSpeed: 3500,
        itemsToShow: 1,
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
