<template>
  <div class="hello">
    <el-button type="primary" @click="show=!show">显示</el-button>
    <transition name="el-zoom-in-top">
      <div v-show="show" style="width: 200px; height: 200px;margin-bottom:20px;background-color: black;"></div>
    </transition>
    <transition name="el-zoom-in-top">
      <div v-show="!show" style="width: 200px; height: 200px;background-color: red;"></div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      show: true,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
