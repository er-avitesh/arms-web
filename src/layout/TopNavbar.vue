<template>
  <div class="container-fluid gradient">
    <nav class="navbar navbar-expand-lg gradient">
      <img
        class=" ls-is-cached lazyloaded"
        style="width:137px;height:71px;"
        src="https://arm-resource.s3.ap-south-1.amazonaws.com/arm-logo.png"
        data-src="https://arm-resource.s3.ap-south-1.amazonaws.com/arm-logo.png"
        alt="ARM Solar"
      />
      <ul class="menu">
        <li @mouseover="listOne = true" @mouseleave="listOne = false">
          <a href="#">Home</a>
        </li>

        <li @mouseover="listTwo = true" @mouseleave="listTwo = false">
          <a href="#">About Us</a>

          <transition name="fade">
            <ul v-if="listTwo" @click="listTwo = false">
              <li><a href="#">About Company</a></li>
              <li><a href="#">Our Partners</a></li>
              <li><a href="#">Mission</a></li>
            </ul>
          </transition>
        </li>

        <li @mouseover="listThree = true" @mouseleave="listThree = false">
          <a href="#">Products</a>

          <transition name="fade">
            <ul v-if="listThree" @click="listThree = false">
              <li><a href="#">Sub Menu Item</a></li>
              <li><a href="#">Sub Menu Item</a></li>
              <li><a href="#">Sub Menu Item</a></li>
            </ul>
          </transition>
        </li>

        <li @mouseover="listFour = true" @mouseleave="listFour = false">
          <a href="#">Contact Us</a>
        </li>
        <li>
          <button class="button button5">Solar Calculator</button>
        </li>
        <li>
          <button class="button button5">Quick Inquiry</button>
        </li>
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  computed: {
    routeName() {
      const { name } = this.$route;
      return this.capitalizeFirstLetter(name);
    }
  },
  data() {
    return {
      listOne: false,
      listTwo: false,
      listThree: false,
      listFour: false
    };
  },
  methods: {
    capitalizeFirstLetter(string) {
      return string.charAt(0).toUpperCase() + string.slice(1);
    }
  }
};
</script>
<style>
.menu {
  font-family: "Yantramanav", sans-serif;
  font-weight: 600;
  margin: 0;
  padding: 0;
  list-style: none;
}

.menu a {
  display: block;
  padding-top: 5px;
  padding-left: 10px;
  color: black;
  font-family: "Open Sans", sans-serif;
  font-size: 16px;
}

.menu li {
  display: block;
  float: left;
  position: relative;
  color: #888888;
  min-width: 160px;
}

.menu li ul {
  position: absolute;
  left: 0;
  top: 55px;
  margin: 0;
  padding: 0;
}

.menu li ul li {
  background: white;
}

.menu li ul li:hover {
  background: #444;
}

/* .fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter,
.fade-leave-active {
  opacity: 0;
} */
.gradient {
  background: white;
}
.button {
  background-color: #4caf50; /* Green */
  border: none;
  color: white;
  padding: 5px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
.button5 {
  border-radius: 12px;
}
</style>
