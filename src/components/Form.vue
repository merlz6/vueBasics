<template>
  <div>
    <input v-model="message" placeholder="edit me">

  <p>This is message:
    {{message}}
  </p>
  </div>

</template>

<script>
  export default {
    name:'Form',
    props:['message']

    }


</script>
