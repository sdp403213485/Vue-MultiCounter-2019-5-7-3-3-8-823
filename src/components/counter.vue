<template>
  <div id="counter">
  <span>{{ index }}</span>
  <button @click="add">+</button>
  <span>{{ number }}</span>
   <button @click="sub">-</button>
</div>
</template>

<script>
export default {
  name: 'counter',


data(){
  return{
    number:0,
  };
},



props:{
  index: Number
},

// created:function(){
//   window.console.log("现在调用created");
// },


methods:{
  clickPlus:function(){
    this.number++;
  },
  clickMun:function(){
    this.number--;
  },

  add: function(){
      this.$emit('count',[this.number,++this.number])
  },
  sub: function(){
      this.$emit('count',[this.number,--this.number])
  }  
  }
};
</script>


<style scoped>
h1{
  font-weight:normal;
}
</style>



