<template>
  <div>
    <mt-swipe :auto="4000">
      <mt-swipe-item v-for="(item, i) in list" :key="i">
        <img :src="item.img" :class="{'full':isfull}">
      </mt-swipe-item>
    </mt-swipe>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: ["list", "isfull"]
};
</script>
<style lang="scss" scoped>
.mint-swipe {
  height: 200px;
  .mint-swipe-item {
    text-align: center;
    img {
      height: 100%;
    }
  }
}
.full {
  width: 100%;
}
</style>