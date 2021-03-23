<template>
  <div class="about">
    <h1>This is some other page page</h1>
    <button >Click for passing from routerviews</button>
  </div>
</template>

<script>
export default {
  name:"AnotherView",
  props:['hello'],
  methods: {function(){
    this.$emit('anotherview', true)
  }
}
}

</script>
