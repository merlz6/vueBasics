<template>
  <div>
    <h1>This is the Footer</h1>
    <b-button @click="clickMe">ClickMe</b-button>
  </div>

</template>

<script>
  export default {
    name:'Footer',
    methods:{
      clickMe(){
        this.$buefy.notification.open('Clicked')
      }
    }
  }

</script>
