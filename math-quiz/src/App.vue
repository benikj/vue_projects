<template>
  <div id="app">
    <h1>Math quiz</h1>
<operator-quiz @onBack="clearOperator" v-if="operator" :operator="operator"></operator-quiz>
    <operator-selector v-if="!operator" @changeOperator="changeOperator">

    </operator-selector>

  </div>
</template>

<script>
import OperatorSelector from "./components/OperatorSelector";
import OperatorQuiz from "./components/OperatorQuiz";

export default {

  name: 'App',
  data(){
    return {
      operator:null
    }
  },
  methods:{
    changeOperator(operator){
      this.operator=operator;
    },
      clearOperator(){
            this.operator=null;
      }
  },
  components: {
    OperatorSelector,
    OperatorQuiz
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
  font-size: 24px;
}
  button{
    padding: 10px;
    width:250px;
    background-color: #10aeb2;
    color: white;
    font-size: 24px;
    cursor: pointer;
    margin-right: 15px;
    height: 80px;
    vertical-align: top;
  }


</style>
