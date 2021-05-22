<template>
  <!DOCTYPE html>
<html lang="fr">
<head>
  <title>Mon Application Vue.js</title>
</head>
<body>
  <div>
      <HelloWorld msg="Welcome to Your Vue.js App"/>
      <Test msg="Welcome to Your Vue.js App"/>
  </div>
</body>
</html>

</template>



<script>
import HelloWorld from './components/HelloWorld.vue'
import Test from './components/Test'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Test
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
  margin-top: 60px;
}
</style>
