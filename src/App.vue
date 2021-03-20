<template>

  <div>
    <blog-head/>
  </div>

</template>



<script>
import header from './components/header.vue'

export default {
  name: 'App',
  components: {
    'blog-head': header
  }
}
</script>

<style>
#app {
  font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin: 0px;
  border: 0px;
}
body{
  border: 0px;
  margin: 0px;
}
</style>
