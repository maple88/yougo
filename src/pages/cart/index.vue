<template>
    <div>
      购物车
    </div>

   
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      list:[
        {
          name:"jack",
          skill:"jump sea"
        },
        {
          name:"rose",
          skill:"eat food"
        },
        {
          name:"robot",
          skill:"tiao hai"
        }
      ]
      
    }
  },



  methods: {
    sayHi(){
      console.log('雷猴啊')
    },
    delect(index){
      this.list.splice(index,1)
    }
  }
}


//  <!-- 如果要配置小程序的window项目需要添加文件main.json   -->
</script>

<style scoped>
  ul li{
    list-style: none;
    width: 750rpx;
    background-color: hotpink;
  }
</style>
