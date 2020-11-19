<template>
  <div id="slider">
    <!-- <transition-group name="fade" tag="div">
    <div class="logo-image" v-for="i in [currentIndex]" :key="i">
      <img :src="currentImg" />
    </div>
    </transition-group> -->
    <div class="logo-image">
      <img :src="image" />
    </div>
  </div>
</template>
<script>
export default {
  name: "Slider",
  data() {
    return {
      images: [
        "https://arm-resource.s3.ap-south-1.amazonaws.com/slide/1.jpg",
        "https://arm-resource.s3.ap-south-1.amazonaws.com/slide/2.jpg"
      ],
      image: "https://arm-resource.s3.ap-south-1.amazonaws.com/slide/1.jpg",
      timer: null,
      currentIndex: 0
    };
  },

  mounted: function() {
    this.startSlide();
  },

  methods: {
    startSlide: function() {
      this.timer = setInterval(this.next, 4000);
    },

    next: function() {
      this.currentIndex += 1;
    },
    prev: function() {
      this.currentIndex -= 1;
    }
  },

  computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    }
  }
};
</script>
<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width: 100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width: 100%;
  opacity: 0;
}

img {
  height: 350px;
  width: 100%;
}

.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.1s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}

.next {
  right: 0;
}

.prev {
  left: 0;
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.9);
}
#slider {
  height: 105px;
  background-color: #eee;
  white-space: nowrap;
  width: 100%;
  display: table;
}

.logo-image {
  vertical-align: middle;
  padding: 2px;
  display: table-cell;
}

.logo-image img {
  max-width: 100%;
}
</style>
