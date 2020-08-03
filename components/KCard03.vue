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
$k-card-02-transition: 0.3s;
$k-box-shadow-01: 0px 2px 2px 0px rgba(117, 117, 117, 0.5),
  0px 1px 2px 0px rgba(117, 117, 117, 0.5);

.k-img-block {
  display: flex;
  flex-direction: column;
  position: relative;
  width: 100%;
  top: -40px;
  box-shadow: $k-box-shadow-01;
  transition: $k-card-02-transition;
}
.k-img {
  height: auto;
  max-width: 100%;
}
.k-content-block {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 40px;
  transition: $k-card-02-transition;
  box-shadow: $k-box-shadow-01;
}
.k-img-block:hover {
  transform: translateY(40px);
}
</style>
