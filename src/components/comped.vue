<!--
 * @Descripttion: 
 * @version: 1.0
 * @Author: 白金鑫
 * @Date: 2020-09-08 19:42:50
 * @LastEditors: 白金鑫
 * @LastEditTime: 2020-09-08 20:13:19
-->
<template>
  <div @click='$emit("isdefale")' class="alert">
      <slot></slot>
      <ul>
          <li v-for="(item,index) in arr" :key="index">

            {{item}}
          </li>
      </ul>
  </div>
</template>

<script>
export default {
    props:{
        arr:Array
    }
}
</script>

<style>
.alert{
    width: 100%;
    height: 100%;
    position: fixed;
    left: 0;
    top: 0;
    background: rgba(0, 0, 0, 0.5);
}

ul{
    width: 200px;
    height: 100px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background: #fff;
    position: absolute;
    left: 50%;
    top: 50%;
    z-index: 5;
    transform: translate(-50%,-50%);
}
</style>