<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>Panier</h2>
    <ul>
      <li>Pommes: {{ costOfApples }}€</li>
      <li>Bananes: {{ costOfBananas }}€</li>
      <li>Noix de coco: {{ costOfCoconuts }}€</li>
    </ul>
    <li>
      <p>Total: {{ total }}€</p>
    </li>
  </div>
</template>

<script>
export default {
  name: "Test",
  props: {
    msg: String,
  },

  

  data () {
    let costOfBananas = 5, 
    costOfApples = 6, 
    costOfCoconuts =  2

    return {
    costOfBananas,
    costOfApples,
    costOfCoconuts,
    total : costOfCoconuts + costOfApples + costOfBananas
    };

  },
  
   function (){
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
</style>
