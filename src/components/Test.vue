<template>
  <div>
    <link type="text/css" rel="stylesheet" href="//unpkg.com/bootstrap/dist/css/bootstrap.min.css" />
    <link type="text/css" rel="stylesheet" href="//unpkg.com/bootstrap-vue@latest/dist/bootstrap-vue.min.css" />
    <h1>{{ msg }}</h1>
    <h2>Panier</h2>
    <ul v-show="state === true">
       <li v-for="item in cost" :key="item" >
            {{item.name}} : {{ item.price }}€
      </li>
    </ul>
  </div>
        <p > Total : {{total()}} € </p>

  <button class="btn btn-primary" v-on:click="alert(cost[0].name)">Button</button>
  <button class="btn btn-primary" v-on:click="hide()">Button</button>
  <p>Ce qu'il y'a écrit dans l'input : {{word}}</p>
  <div class="input-group input" >
    <input class="form-control" v-model="word">
  </div>
</template>

<script >

export default {
  name: "Test",
  props: {
    msg: String,
  },

  data () {

    return {
    cost: [
                { name: 'Bananas', price: 5 },
                { name: 'Apples', price: 6 },
                { name: 'Coconuts', price: 2 }
            ],
    
    word  : '',
    state : true

    }

  
  },



  methods: {
    alert(a){
      alert(a)
    },

    log(){
      console.log('hey');
    },

    total(){
      let total  = 0
      this.cost.forEach(item => {
        total += item.price
      });
       return total
    },

    hide(){
      if(this.state ==true ){
        this.state = false
      }
      else{
        this.state = true
      }

      console.log(this.state);

    }
    



 

  },

  
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.input{
  width: 80%;
  margin: 0 auto;
  margin-top: 2%;
}


</style>
