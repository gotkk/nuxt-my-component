<template>
  <div class="k-card-03">
    <div class="k-content-block">
      <span>{{ imgTitle }}</span>
    </div>
    <div class="k-img-block">
      <img :src="imgUrl" class="k-img" :alt="imgTitle" />
    </div>
  </div>
</template>

<script>
export default {
  name: "KCard03",
  props: {
    imgUrl: {
      type: String,
      default: "_nuxt/assets/icon.png"
    },
    imgTitle: {
      type: String,
      default: "Title is not available"
    }
  }
};
</script>

<style lang="scss" scoped>
$k-card-03-transition: 0.3s;
$k-box-shadow-01: 0px 2px 2px 0px rgba(117, 117, 117, 0.5),
  0px 1px 2px 0px rgba(117, 117, 117, 0.5);

.k-card-03 {
  width: 100%;
  position: relative;
  cursor: pointer;
  transition: $k-card-03-transition;
}
.k-img-block {
  display: flex;
  flex-direction: column;
  position: relative;
  padding: 6px;
  width: 100%;
  top: -40px;
  box-shadow: $k-box-shadow-01;
  background-color: #ffffff;
  transition: $k-card-03-transition;
}
.k-img {
  max-width: 100%;
  height: auto;
}
.k-content-block {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 40px;
  transition: $k-card-03-transition;
  box-shadow: $k-box-shadow-01;
}
.k-img-block:hover {
  transform: translateY(40px);
}
</style>
