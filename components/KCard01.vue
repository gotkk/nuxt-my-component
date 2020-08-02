<template>
  <div class="k-card-01">
    <img :src="imgUrl" class="k-img" :alt="imgTitle" />
    <div class="k-title-block">
      <span class="k-text">{{ imgTitle }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "KCard01",
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
$k-card-01-transition: 0.3s;

.k-card-01 {
  display: flex;
  width: 100%;
  position: relative;
  cursor: pointer;
  transition: $k-card-01-transition;
}
.k-card-01:hover {
  box-shadow: 0 0 10px 6px #3a3a3a;
  transform: scale(1.05);
}
.k-card-01::after {
  content: "\A";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  opacity: 1;
  transition: $k-card-01-transition;
}
.k-card-01:hover::after {
  opacity: 0;
  // box-shadow: 0 0 10px 6px #3a3a3a;
  // transform: scale(1.05);
}

.k-card-01 .k-img {
  max-width: 100%;
  height: auto;
}
.k-card-01 .k-text {
  color: #ffffff;
}

.k-card-01 .k-title-block {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  transition: $k-card-01-transition;
  font-size: 20px;
}
.k-card-01 .k-title-block:hover {
  opacity: 0;
}
</style>
