<template>
  <div>
    <h1>This is the Footer</h1>
    <b-button @click="clickMe">ClickMe</b-button>
    <h1>API CALL FROM APP.vue</h1>
    {{info}}
  </div>

</template>

<script>
  export default {
    name:'Footer',
    props:['info'],
    methods:{
      clickMe(){
        this.$buefy.notification.open('Clicked')
      }
    }
  }

</script>
