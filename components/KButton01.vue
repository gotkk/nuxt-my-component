<template>
  <div class="k-button-01" @click="$emit('btnClick')">
    <div class="block-text">
      <span class="text">{{text}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "KButton01",
  props: {
    text: {
      type: String,
      default: "KButton"
    }
  },
};
</script>

<style lang="scss" scoped>
.k-button-01 {
  background-color: rgba(0,0,0,0.2);
  width: 100%;
  height: 100%;
  border: 1px solid;
  color: #000000;
}
.k-button-01:hover{
    background-color: rgba(0,0,0,0.8);
    color: #ffffff;
    cursor: pointer;
}
.block-text{
    width: 100%;
    height: 32px;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>