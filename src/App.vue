<template>
  <router-view/>
</template>

<script>
import { provide } from "vue"
import * as echarts from "echarts"
import axios from "axios"
// 设置axios基准路径
axios.defaults.baseURL = "http://127.0.0.1:8888"
export default {
  setup() {
    provide("echarts", echarts)
    provide("axios", axios)
  }
}
</script>

<style lang="less">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background: url("~@/assets/bg.jpg") top center no-repeat;
}
</style>
