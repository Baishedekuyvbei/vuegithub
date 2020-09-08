<!--
 * @Descripttion: 
 * @version: 1.0
 * @Author: 白金鑫
 * @Date: 2020-09-08 17:51:04
 * @LastEditors: 白金鑫
 * @LastEditTime: 2020-09-08 20:14:26
-->
<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    vue
    <comped :arr='arr' v-if="flag" @isdefale="flag=false" :title.sync='title' >
        <h1>{{title}}</h1>
    </comped>
    <button @click="flag=true">
        点击
    </button>
    
  </div>
</template>

<script>
    import comped from './components/comped'

export default {
  name: 'App',
  components: {
      comped
  },
  data(){
      return {
          flag:false,
          arr:['开心','不开心'],
          title:'你开心吗？'
      }
  },
}
</script>

<style>
h1{
    font-size: 36px;
}
*{
    
    list-style: none;
}
</style>
