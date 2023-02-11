<script setup>
import{ref} from "vue"; 

import Thetodos from "./components/Thetodos.vue";



var name=ref("mhdi");

var todos=ref([
  {
    title:"HI HI",
    is_done:true
  },
  {
    title:"NOUHA",
    is_done:false
  },
  {
    title:"LAAOUINA",
    is_done:false
  },
])
const addTodo=()=>{
  todos.value.push({
    title:name.value,
    is_done:false
  })
}

</script>

<template>
<div class="app">
  <div class="content">
    <Thetodos :todos="todos"/>
    <p>{{name}}</p>

  </div>
  <div class="zone">
<input v-model="name" type="text" name="tod" class="input1">
<button class="btn" @click="addTodo">add</button>
  </div>
</div>
</template>

<style scoped>
*{
  margin:0;
  padding:0;

}
.app{
  display: grid;
  justify-content: center;
  align-items: center;
  height:100vh;

}
.btn{
  border-radius: 5px;
}
</style>
