<template>
  <div class="k-card-02">
    <div class="k-img-block">
      <img :src="imgUrl" class="k-img" :alt="imgTitle" />
    </div>
    <div class="k-back-content-block">
      <span class="k-text">{{ imgTitle }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardHover02",
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
$k-card-02-transition: 0.7s;
$k-box-shadow-01: 0px 2px 2px 0px rgba(117, 117, 117, 0.5),
  0px 1px 2px 0px rgba(117, 117, 117, 0.5);

.k-card-02 {
  width: 100%;
  position: relative;
  cursor: pointer;
  transition: $k-card-02-transition;
}
.k-card-02:hover {
  transform: rotateY(180deg);
  transition: $k-card-02-transition;
}
.k-back-content-block {
  transform: rotateY(180deg);
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  font-size: 20px;
}
.k-back-content-block:hover {
  opacity: 1;
  transition: $k-card-02-transition;
}
.k-img-block {
  width: 100%;
  height: auto;
  padding: 6px;
  background-color: #ffffff;
  box-shadow: $k-box-shadow-01;
}
.k-img {
  max-width: 100%;
  height: auto;
}
.k-text {
  color: #ffffff;
}
</style>
