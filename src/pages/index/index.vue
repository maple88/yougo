<template>
    <div>
      <input type="button" value="点我啊" @click="sayHi">
      <ul>
        <li v-for="(item,index) in list" :key="index" @longtap="delect(index)">
          姓名:{{item.name}} ---  技能:{{item.skill}}
        </li>
      </ul>
    
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
