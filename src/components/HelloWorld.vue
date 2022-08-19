<template>
  <div class="hello">
    <el-button type="primary" @click="showBoxB = !showBoxB">显示</el-button>
    <div class="tran_warp">
      <div :style="`width: 200px; height: 200px;margin-bottom:20px;background-color: black;`" class="box" :class="{'mvBox':showBoxB}"></div>
      <div :style="`width: 200px; height: 200px;background-color: red;`" class="box" :class="{'mvBox':showBoxB}"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      showBoxB: false,
      animationName: ""
    };
  },
  methods: {}
};
</script>

<style lang="less">
.hello {
  .tran_warp {
    width: max-content;
    height: 200px;
    overflow: hidden;
  }
  .box {
    transition: transform 0.5s ease-out;
  }
  .mvBox {
    transform: translateY(-220px);
  }
}
</style>
