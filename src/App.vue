<template>
  <div id="app" class="shane_tm_all_wrap">
    <router-view></router-view>
    <back-top color="#fff" :size="1.2" bottom="5%" :slow="0"> </back-top>
  </div>
</template>

<script>
export default {
  mounted() {
    document.body.classList.add("loaded");
  },
  destroyed() {
    document.body.classList.remove("loaded");
  },
};
</script>

<style lang="scss">
.back-top {
  z-index: 99;
}
.back-top__icon {
  color: #000 !important;
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.15) !important;
  border-radius: 4px !important;
  font-size: 20px !important;
}
</style>
