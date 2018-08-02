<template>
    <div>
    <button class="ui-button" @click="addCount">{{text}}</button>
    <p>按钮被点击了{{count}}次</p>
    </div>
</template>
<script>
    export default {
        name:"myButton",
        data:function(){
          return{
            "message":"my first component",
            "count":0
          }
        },
        methods:{
          "addCount":function(){
            this.count ++;
            this.$emit("add");
          }
        },
        props:{
          'text':{
            type:String,
            required:true
          }
        }
    }
</script>
<style>
.ui-button{
  background-color:blue;
  color:white;
  border:none;
}
</style>
