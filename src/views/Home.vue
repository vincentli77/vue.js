<template>   <!DOCTYPE html>
<html lang="fr">
<head>
  <title>Mon Application Vue.js</title>
</head>
<body>
  <div>
      <HelloWorld @parent-click="klik" msg="Welcome to Your Vue.js App"/>
  </div>
  <h1>{{this.msg}}</h1>
</body>
</html>

</template> 

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
  },

  data(){
    return {
      msg : ''
    }
  },

  methods : {
    klik(a){
            this.msg = a.msg
            console.log(this.msg);
    }
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
color: #2c3e50;
  margin-top: 60px;
color: #2c3e50;
  margin-top: 60px;
}
</style>