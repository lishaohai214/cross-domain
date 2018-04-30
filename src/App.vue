<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import axios from 'axios'
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  created(){
      // fetch
      // fetch('/apis/test/testToken.php',{
      //   method:"post",
      //   headers:{
      //     "Content-type":"application/json",
      //     token:"f4c902c9ae5a2a9d8f84868ad064e706"
      //   },
      //   body:JSON.stringify({username:"henry",password:"1234"})
      // })
      // .then((result) => {
      //   // console.log(result)
      //   return result.json();
      // } )
      // .then(res => console.log(res))
      // .catch( err => console.log(err));

      // this.$axios.post('/apis/test/testToken.php',{ username:"hello",password:"123456"})
      // .then(data=>console.log(data))
      
      let instant = axios.create({
        baseURL:'/apis',
        headers:{"Content-type":"application/json",
         token:"f4c902c9ae5a2a9d8f84868ad064e706"}
      instant.post('/test/testToken.php',{ username: 'mynae',password:'1111' }).then((data)=>{console.log(data)}
      
      
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
