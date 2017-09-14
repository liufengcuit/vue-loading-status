<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <loading :com='compelete'></loading>
  </div>
</template>

<script>
import Loading from './Loading.vue'
export default {
  name: 'hello',
  components:{ Loading },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      compelete:10
    }
  },
  methods:{
    counTime:function(){
      var that = this;
      var time = setInterval(function(){
        that.compelete--;
      },100);
    }
  },
  mounted (){
    // this.counTime();
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
