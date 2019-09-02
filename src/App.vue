<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <input v-model="num"/>
    <counter @count="count" v-for="n in +num" v-bind:key="n"  v-bind:index="n"/>
    <span>sum:{{sum}}</span>
  </div>
</template>

<script>
import counter from './components/counter.vue'
export default {
  name: 'app',
  components: {
    counter
  },



data(){
  return{
    num:0,
    sum:0
    };
  },


methods:{
  count: function (e) {
    this.sum = this.sum -e[0]+e[1]
  }

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
