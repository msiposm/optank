<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inconsolata&family=Open+Sans:ital,wght@0,400;1,400&display=swap');

#app {
  /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
  font-family: 'Open Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: white;
  /*margin-top: 60px;*/
}

body {
  background: rgb(24, 24, 24);
  padding: 0px;
  margin: 0px;
}
</style>
