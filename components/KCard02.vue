<template>
    <div class="k-card-02">
      <img :src="imgUrl" class="k-img" :alt="imgTitle" />
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
$k-card-02-transition: 0.7s;

.k-card-02 {
  display: flex;
  width: 100%;
  transition: $k-card-02-transition;
  position: relative;
  cursor: pointer;
}
.k-card-02:hover {
  transform: rotateY(180deg);
  transition: $k-card-02-transition;
}
.k-card-02 .k-back-content-block {
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
.k-card-02 .k-back-content-block:hover {
  opacity: 1;
  transition: $k-card-02-transition;
}
.k-card-02 .k-img {
  max-width: 100%;
  height: auto;
}
.k-card-02 .k-text {
  color: #ffffff;
}
</style>
