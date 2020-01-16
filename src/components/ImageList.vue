<template>
    <div class="image-list">
        <div class="center">
            <div v-for="(item,index) in list" :key="index" class="img-item">
                <img :src="item.url" alt="">
                <div class="title">
                    {{'标题：《'+ item.title +'》'}}
                </div>
                <div class="auth">
                    {{'作者：'+ item.auth}}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'imageList',
    props:{
        list: Array
    },
    data(){
        return{

        }
    },
}
</script>
<style lang="scss" scoped>
.image-list{
    .center{
        overflow-y: auto;
        .img-item{
            box-shadow: 0 3px 20px #888888;
            border-radius: 3px;
            float: left;
            width: 165px;
            height: 300px;
            background: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            img{
                width: 165px;
                height: 200px;
            }
            &:nth-child(odd){
                margin: 0 15px 10px 0;
            }
            .title{
                margin: 10px 0 10px;
            }
        }
    }
    
}
</style>