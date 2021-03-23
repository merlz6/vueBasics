<template>
  <div>
    <h1>Hello</h1>
    <h2>{{cheese}}</h2>
    <HelloWorld  v-bind:cheese="cheese"/>
    <button v-on:click="handleClick">Click Me</button>


  </div>

</template>


<script>
import HelloWorld from "./components/HelloWorld.vue"



export default {
  name: 'App',
  data:function(){
    return{
        cheese:"gouda"
    }
  },
  components:{HelloWorld},
  methods:{
    handleClick:function(){
      this.cheese = "munster"
    }
  }
}
</script>


<style>
h1 {
  color: red;
}
</style>
