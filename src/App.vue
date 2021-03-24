<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
        <router-link :to="{name:'AnotherView', query:{hello:this.hello}}" >AnotherView</router-link>
    </div>
    <Header v-bind:hello="hello" @test="handleTest($event)"/>
    <router-view @home="handleHome($event)"/>
    <Carousel />
    <Footer v-bind:info="info"/>
    <h1>API CALL:</h1>
      {{info}}

      <Form message="message"/>
      <p>
        {{message}}
      </p>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Carousel from './components/Carousel.vue'
import Form from './components/Form.vue'
import axios from 'axios'
  export default {
    name:'App',
    components:{
      Header,
      Footer,
      Carousel,
      Form
    },
    methods:{
      handleTest:function(event){
        console.log(event)
      },
      handleHome:function(event){
        console.log(event)
      }
    },
    data:function(){
      return {
        hello:'World',
        info:null,
        message:''
      }
    },
    mounted(){
      axios
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => (this.info = response.data.bpi))
    }
  }

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
