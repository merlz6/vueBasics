<template>
  <div>
    <h1>Goodbye</h1>
    <h2>{{cheese}}</h2>
  </div>

</template>


<script>
export default {
  name: 'HelloWorld',
  props:['cheese']
}
</script>


<style>
h1 {
  color: red;
}
</style>
