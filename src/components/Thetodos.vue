<script setup>
import {ref} from "vue";


defineProps({
    todos:[]
})


// const changeTodo = (todo)=>{
//     todo.value.push({
//     is_done:true
//   })
// }

</script>
<template>
    <ul>
    <h3>To Do</h3> 

    
  
  <div v-for="todo in todos" :key="todo.value" class="todo" >
  <div v-if="todo.is_done==false" class="done">
    <input  type="checkbox" >
   {{  todo.title}}
   {{ todo.is_done }}
</div>

   
</div>
<hr>
<h3>Done</h3>


  <div v-for="todo in todos" :key="todo.value" class="todo">
  <div v-if="todo.is_done==true" class="done">
   
   {{  todo.title}}
   {{ todo.is_done }}
</div>
</div>
</ul>
</template>
<style>
.todo{
    border:1px solid;
    background-color: rgb(85, 171, 85);
    color:white;
    
}
.done{
    padding:10px 22px;
    font-family:Arial, Helvetica, sans-serif;
}
h3{
    font: optional;
}
</style>