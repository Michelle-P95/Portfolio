<template>
  <div class="about_inner">
    <div class="left">
      <div class="image">
        <img src="" alt="placeholder" />
        <div
          class="main"  
          :style="{ backgroundImage: 'url(' + aboutImg + ')' }"
          @mouseover="changeAboutImg"
          @mouseleave="resetAboutImg"
             
        ></div>
      </div>
      <!-- End image  -->
    </div>
    <!-- End left -->

    <div class="right">
      <div class="shane_tm_title">
        <span >About Me</span>
       <!--  <h3 v-scroll-reveal="{ delay: 40 }">Me</h3> -->
      </div>
      <div class="text" >
        <p>My Idealism gets me to my Mindset which is about treating myself like a computer. I am constantly updating my body and
        mind through nutrition, sports, and self-development. <br>
        <br>
        My love for video games as a child led me to pursue a career in
        the field of computer science. The wide range of my interests brings me to always learning new skills which expands my
        tool box for creating digital products. <br>
        Psychology which is one of my biggest Interests, was my main course in high
        school, brings me to my never ending analysing and thinking about how to create a product for the best possible human
        experience. 
        <br><br>
        --> because that's what i want to ensure, using technology for bettering our Human Life !
        
        <i style="color:limegreen;">my favorite questions are <bold>HOW</bold> & <bold>WHY</bold> ?</i>

<!-- style="color:rgb(115, 162,43);  -->
       
</p>
<br>       
      </div>
      <div class="shane_tm_button" >
        <a href="/CV_Poetsch_Michelle.pdf" download> Download CV </a>
      </div>
    </div>
    <!-- End right -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      aboutImg: require("../../assets/img/Ich/normal1.jpg"),
      newImg: require("../../assets/img/Ich/3.jpg"),
    };
  },
  methods: {
    changeAboutImg() {
      this.aboutImg = this.newImg;

    },
    resetAboutImg() {
      this.aboutImg = require("../../assets/img/Ich/normal1.jpg");
    
    }
  }
};
</script>
