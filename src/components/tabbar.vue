<template>
    <div>
    <mt-tabbar @click.native="tabbarGo()" v-model="selected">
      <mt-tab-item id="">
        <img slot="icon" src="../assets/tabbar1.png">
        表情包
      </mt-tab-item>
      <mt-tab-item id="search">
        <img slot="icon" src="../assets/tabbar2.png">
        搜索
      </mt-tab-item>
      <mt-tab-item id="person">
        <img slot="icon" src="../assets/tabbar3.png">
        我的
      </mt-tab-item>
    </mt-tabbar>
</div>
</template>
<script>
export default {
    name:'tabbar',
    props: {
        nowBar: String
    },
    data(){
        return {
            selected: this.nowBar
        }
    },
    methods:{
        tabbarGo(){
            console.log(this.nowBar)
            console.log(this.selected)

            if(this.nowBar !== this.selected){
                this.$router.push({
                    path: `/${this.selected}`
                })
            }
        }
  }
}
</script>>