<template>
  <div class="k-card-04">
    <div class="k-img-block">
      <img :src="imgUrl" class="k-img" :alt="imgTitle" />
    </div>
    <div class="k-title-block">
      <span class="k-text">{{ imgTitle }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "KCard04",
  props: {
    imgUrl: {
      type: String,
      default: "../assets/1.jpg"
    },
    imgTitle: {
      type: String,
      default: "Title is not available"
    }
  }
};
</script>

<style lang="scss" scoped>
$k-card-04-transition: 0.3s;
$k-box-shadow-01: 0px 2px 2px 0px rgba(117, 117, 117, 0.5),
  0px 1px 2px 0px rgba(117, 117, 117, 0.5);

.k-card-04 {
  width: 100%;
  position: relative;
  cursor: pointer;
  transition: $k-card-04-transition;
}
.k-img-block {
  width: 100%;
  height: auto;
  padding: 6px;
  background-color: #ffffff;
  box-shadow: $k-box-shadow-01;
}
.k-title-block {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  background-color: rgba(0, 0, 0, 0.5);
  transition: $k-card-04-transition;
  opacity: 0;
}
.k-title-block:hover {
    opacity: 1;
}
.k-img {
  max-width: 100%;
  height: auto;
  cursor: pointer;
  background-color: #ffffff;
}
.k-text{
    color: #ffffff;
    font-size: 20px;
}
</style>
