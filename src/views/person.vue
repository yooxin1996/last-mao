<template>
  <div class="">
    <img src="../assets/dm.jpg" alt="">
    <h1>还没做喔 ^_^</h1>
    <tabbar :nowBar="select"></tabbar>

  </div>
</template>
<script>
import tabbar from '../components/tabbar'

export default {
   ata(){
    return {
      select: ''
    }
  },
   components: {
    tabbar
  },
  created(){
    this.select = 'person'
  }
}
</script>
<style lang="scss" scoped>

</style>