<template>
  <div id="app">
    <Alunos/> 
  </div> 
  
</template>

<script>
import Alunos from './components/Alunos.vue'

export default {
  name: 'app',
  components: {
    Alunos
  }
}
</script>

<style>
body{
  background-color: #eee;
  display: grid;
  justify-items: center;
}

body,html {
  margin: 0;
  height: 100%;
}

#app {
  
}
.btn-Danger{
  background-color: #fa4430;
}
.btn{
  padding: 10px 20px;
  cursor: pointer;
  border: 1px solid #000;
  color: white;
  font-weight: bold;
  border-radius: 5px;
  border-bottom: 3px solid #000;
  border-right: 3px solid #000;
  border-left: 3px solid #000;
}
.btn:hover{
  text-shadow: 1px 1px 1px black;
  margin-top: 3px;
  border-bottom: 1px solid black;
  border-right: 1px solid #000;
  border-left: 1px solid #000;
}

table{
  margin: 0px;
  padding: 0px;
  list-style-type: none;
  width: 100%;
  border: none;
  font-weight: bold;
}

table th {
  background-color: rgb(22, 170, 219) !important;
  font-size: 1.2em;
  padding: 10px 0px;
  text-align: center;
}

tr td {
  padding: 20px;
  font-size: white;
  background-color: #aec5c9;
  margin-bottom: 2px;
  color: #3e5252;
  text-align: center;
}

.colPequeno{
  width: 5%;
}

</style>
