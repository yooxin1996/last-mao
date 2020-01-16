<template>
  <div>
    <img src="../assets/dm.jpg" alt="">
    <h1>还没做喔 >_< </h1>
    <tabbar :nowBar="select"></tabbar>

  </div>
</template>
<script>
import tabbar from '../components/tabbar'

export default {
  data(){
    return {
      select: ''
    }
  },
   components: {
    tabbar
  },
  created(){
    this.select = 'search'
  }
}
</script>
<style lang="scss" scoped>

</style>