<template>
  <div class="row">
    <div class="col">
      <img :src="waree" />
    </div>
    <div class="col">
      <img :src="waacab" />
    </div>
    <div class="col">
      <img :src="luminous" />
    </div>
    <div class="col">
      <img :src="okaya" />
    </div>
  </div>
</template>
<script>
export default {
  name: "Partners",
  data() {
    return {
      waacab:
        "https://arm-resource.s3.ap-south-1.amazonaws.com/partners/waacab-logo.png",
      luminous:
        "https://arm-resource.s3.ap-south-1.amazonaws.com/partners/luminous-logo.jpg",
      waree:
        "https://arm-resource.s3.ap-south-1.amazonaws.com/partners/Waaree-logo.png",
      okaya:
        "https://arm-resource.s3.ap-south-1.amazonaws.com/partners/Okaya-Logo.png"
    };
  }
};
</script>
<style scoped>
img {
  height: 80px;
  width: 100%;
}

#partner {
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
</style>
