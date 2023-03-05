<template>
  <div class="shane_tm_intro shane_error_page">
    <div class="hero" :style="{ backgroundImage: 'url(' + imgSrc + ')' }">
      <div class="content">
        <h1>404!</h1>
        <p>The page you are looking for could not be found.</p>

        <router-link class="white-fill-bg btn-outline" to="/">
          BACK TO HOME
        </router-link>
        <!--  End purchase_button -->
      </div>
    </div>
    <!-- End .hero -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgSrc: require("../assets/img/patterns/1.png"),
    };
  },
};
</script>

<style lang="scss" scoped></style>
