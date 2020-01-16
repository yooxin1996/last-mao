<template>
  <div class="home">
    <div class="home-header">
      <div>
        <img src="../assets/dm.jpg" alt="">
        <img :src="'../assets/sucai/1.jpg'" alt="">

      </div>
      <div class="header-text">
        <p>如果让你重新来过，你会不会爱我。 <br/>—— LastMao</p>  
      </div>
    </div>

    <a href="https://github.com/yooxin1996" target="blank" style="text-decoration:none">
      <div class="header-tips">
          <img src="../assets/laba.png" alt="">
        <div class="tips">
          蛋八，永远滴神！(长按图片保存)
        </div>
      </div>
    </a>

    <div class="content" :style="{height: scrollerHeight}">
      <imageList :list="imgList"></imageList>
    </div>

  <tabbar :nowBar="select"></tabbar>
    
  </div>
</template>

<script>
// @ is an alias to /src
import tabbar from '../components/tabbar'
import imageList from '../components/ImageList'


export default {
  name: 'home',
  data(){
    return {
      select: '',
      imgList: [{
        url: require('../assets/sucai/1.jpg'),
        title: '奥秘毛',
        auth: '包哥'
      },{
        url: require('../assets/sucai/2.jpg'),
        title: '棉被毛',
        auth: '包哥'
      },{
        url: require('../assets/sucai/3.jpg'),
        title: '猪儿虫毛',
        auth: '包哥'
      }]
    }
  },
  components: {
    tabbar,
    imageList
  },
  methods:{
    
  },
  created(){
    this.select = ''
  },
  computed: {
    scrollerHeight: function() {
      return (window.innerHeight - 200) + 'px';
    }
  }
}
</script>

<style lang="scss">
.home{
  width: 100%;
  height: 100%;
}
.home-header{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 60px;
  background: #fff;
  display: flex;
  align-items: center;
  padding-left: 30px;
  box-sizing: border-box;
  border:1px solid transparent;
  margin-bottom: 20px;
  img{
    width: 30px;
    height: 40px;
  }
  .header-text{
    font-size: 14px;
    margin-left: 40px;
  }
}
.header-tips{
  margin: 80px 0 15px 0;
  width: 100%;
  height: 25px;
  background: rgba($color: #555, $alpha: .7);
  font-size: 12px;
  display: flex;
  align-items: center;
  padding-left: 15px;
  box-sizing: border-box;
  img{
    width: 15px;
    height: 15px;
  }
  .tips{
    color: #fff;
    margin-left: 15px;
  }
}
.content{
  overflow: auto;
  padding: 15px;
}
</style>
