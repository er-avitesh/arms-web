<template>
  <div class="wrapper">
    <div>
      <Header></Header>
      <top-navbar></top-navbar>
      <slider></slider>
      <partners></partners>
      <!-- <balloon></balloon> -->
    </div>
  </div>
</template>
<style lang="scss">
.slider {
  height: 310px;
  width: 1910px;
}
.column {
  float: left;
  width: 50%;
  padding: 10px;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
</style>
<script>
import TopNavbar from "./TopNavbar.vue";
import DashboardContent from "./Content.vue";
import Header from "./Header.vue";
import Slider from "./Slider.vue";
import balloon from "./balloon.vue";
import partners from "./partners.vue";
export default {
  components: {
    Header,
    TopNavbar,
    DashboardContent,
    Slider,
    partners,
    balloon
  },
  methods: {}
};
</script>
