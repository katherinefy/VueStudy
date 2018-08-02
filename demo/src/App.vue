<template>
  <div id="app">
    <img src="./assets/logo.png">
    <firstComponents text="计数" @add="addCount"></firstComponents>
    <firstComponents text="计数" @add="addCount"></firstComponents>

    <p>按钮被点击的总次数：{{totalCount}}</p>
  </div>
</template>

<script>
import myButton from './components/Buttons/Button'

export default {
  name: 'App',
  data:function(){
       return{
             "totalCount":0
           }
         },
  methods:{
    "addCount":function(){
      this.totalCount++;
    }
  },
  components:{
    "firstComponents":myButton
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
