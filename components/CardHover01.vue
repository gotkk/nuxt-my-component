<template>
  <div class="card-hover-01">
    <div class="k-hover-card1">
      <img :src="imgUrl" class="k-img" :alt="imgTitle" />
      <div class="k-title-block">
        <span class="k-text">{{imgTitle}}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardHover01",
  props: {
      imgUrl: {
          type: String,
          default: "../assets/1.jpg"
      },
      imgTitle: {
          type: String,
          default: "Title is not available"
      }
  },
};
</script>

<style lang="scss" scoped>
$hover-card1-transition: 0.3s;

.k-hover-card1 {
  display: flex;
  width: 100%;
  position: relative;
  cursor: pointer;
  transition: $hover-card1-transition;
}
.k-hover-card1:hover {
  box-shadow: 0 0 10px 6px #3a3a3a;
  transform: scale(1.05);
}
.k-hover-card1::after {
  content: "\A";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  opacity: 1;
  transition: $hover-card1-transition;
}
.k-hover-card1:hover::after {
  opacity: 0;
  // box-shadow: 0 0 10px 6px #3a3a3a;
  // transform: scale(1.05);
}

.k-hover-card1 .k-img {
  max-width: 100%;
  height: auto;
}
.k-hover-card1 .k-text {
  color: #ffffff;
}

.k-hover-card1 .k-title-block {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transition: $hover-card1-transition;
  font-size: 20px;
}
.k-hover-card1 .k-title-block:hover {
  opacity: 0;
}
</style>
