<template>
  <div>
    <balloon title="Quick Inquiry" position="bottom-right">
      <inquiry></inquiry>
    </balloon>
  </div>
</template>
<style scoped>
.inquiry {
  height: 100%;
}
</style>
<script>
import { Balloon } from "vue-balloon";
import inquiry from "./inquiry.vue";
export default {
  components: { Balloon, inquiry },

  methods: {
    // @maximize="playVideo"
    //   @minimize="pauseVideo"
    // playVideo() {
    //   this.$refs.player.player.playVideo();
    // },
    // pauseVideo() {
    //   this.$refs.player.player.pauseVideo();
    // }
  }
};
</script>
