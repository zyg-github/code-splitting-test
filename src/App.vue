<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div><router-link to="/hello">Hello</router-link></div>
    <router-view></router-view>
  </div>
</template>

<script>
// import axios from 'axios'
export default {
  name: 'app',
  created () {
    axios.get('https://www.baidu.com/')
    .then(function (response) {
      console.log(response);
    })
    .catch(function (error) {
      console.log(error);
    });
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
