<template>
<!-- 跑马灯背景 -->
  <div class="el-carousel__counter">
    <el-carousel height="100vh" indicator-position="none" interval="2000">
      <el-carousel-item v-for="header in bg" :key="header">
        <el-image :src="header.url" :alt="header.name" fit="cover" hide-on-click-modal="true" style="width:100vw; height:100vh;"/>
      </el-carousel-item>
    </el-carousel>
  </div>

  <!-- 推荐文章 -->

  <!-- 联系方式 -->

  <!-- footer -->

</template>

<script>
export default {
  name: "home",
  data() {
      return {
        bg: [
          {name: 'background_1', url: require('../assets/img/bg_1.png')},
          {name: 'background_2', url: require('../assets/img/bg_2.png')},
          {name: 'background_3', url: require('../assets/img/bg_3.png')},
          {name: 'background_4', url: require('../assets/img/bg_4.png')},
          {name: 'background_5', url: require('../assets/img/bg_5.png')},
          {name: 'background_6', url: require('../assets/img/bg_6.png')},
          {name: 'background_7', url: require('../assets/img/bg_7.png')},
          {name: 'background_8', url: require('../assets/img/bg_8.png')},
          {name: 'background_9', url: require('../assets/img/bg_9.png')},
          {name: 'background_10', url: require('../assets/img/bg_10.png')},
        ]
      }
    }
}
</script>

<style scoped>
.test{
  color:rgb(197, 70, 31)
}
/* 跑马灯样式 */
.el-carousel__counter{
  height: 100vh;
  width: 100%;
  justify-items: center;
  z-index: -1;
  height: 100vh; 
  position: absolute;
}

</style>