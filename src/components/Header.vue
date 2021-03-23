<template>
  <div>
    <h1>This is the Header</h1>
    <button @click="test">Click to Test passing info</button>

  </div>

</template>

<script>
  export default {
    name:'Header',
    props:['hello'],
    methods:{
      test:function(){
        this.$emit("test", 5)
      }
    }
  }

</script>
