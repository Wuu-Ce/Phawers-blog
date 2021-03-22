<template>  
  <div class="mainflex">

    <div class="mainBox">
      <router-link to="/home" replace><i class="el-icon-present item-1">Phawers' blog</i></router-link>
      <div class="item-emptybox"></div>

      <div class="linkcounter">
        <router-link v-for="option in options" :to="option.src" class="items" :key="option">
          <i :class="option.icon">{{option.name}}</i>
        </router-link>
      </div>
        
    </div>

    <router-view style="order: 2;"/>  

  </div>

</template>


<script>
export default {
  name: "header",
  data() {
    return {
      options: [
        {
          name: '主页',
          src: '/home',
          icon: 'el-icon-s-home'
        },
        {
          name: '文章',
          src: '/artical',
          icon: 'el-icon-notebook-2'
        },
        {
          name: '关于',
          src: '/about',
          icon: 'el-icon-more'
        }
      ]
    }
  },
}
</script>

<style scoped>
.mainflex{
  display: flex;
  display: -webkit-flex;
  width: 100%;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: center;
  border: 0px;
}

.mainBox{
  order: 0;
  width: 100%;
  height: 50px;
  display:flex;
  background-color: rgba(51, 48, 48, 0.5);
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  border-style: outset;
  border-width: 2px;
  border-color: rgba(2, 2, 2, 0.5);
}
.item-1{
  order: -1;
  width: 12em;
  padding-left: 8px;
  font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
  color: rgb(255, 255, 255);
  font-size: 1.5em;
}
.item-emptybox{
  order: 1;
  width: 1fr;

  flex-shrink: 0.5;
}
.linkcounter{
  order: 2;
  display:flex;
  justify-items: center;
  width: 15em;
}

.items{
  width: 4em;
  font-family: "微软雅黑",Arial,sans-serif;
  color:rgb(230, 217, 238);
  font-size: 16px;
  text-decoration: none;
}
.items:active{
  color: rgb(101, 207, 221);
}


</style>