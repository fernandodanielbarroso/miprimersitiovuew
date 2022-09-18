<script setup>
import {ref,computed} from 'vue'
const counter=ref(0)
const incremento=()=>{
  console.log('aumentar contador')
  counter.value+++
  console.log(counter.value)
}

const disminuirContador=()=>{
  console.log('aumentar contador')
  counter.value--
  console.log(counter.value)
}
const resetear=()=>{
  
  counter.value=0
  
}
const classCounter=computed(
  ()=>{
     if(counter.value===0){
      return "zero";
     }  
     if(counter.value>0){
      return "positive"
     }
     if(counter.value<0){
      return "negative"
     }
  }
);
const classCounter2=()=>{
  if(counter.value===0){
      return "zero";
     }  
     if(counter.value>0){
      return "positive"
     }
     if(counter.value<0){
      return "negative"
     }
}
const arrayFavoritos=ref([])

const add=()=>{
  arrayFavoritos.value.push(counter.value)
}
const bloquear=computed(
  ()=>{
    const numSearch=arrayFavoritos.value.find(num=>num===counter.value)
   // console.log(numSearch) 
    //if(numSearch==0)
     // return true  
    //return numSearch?true:false
    return numSearch || numSearch===0
  }

)
</script>

<template>
  <div class="container text-center mt-3" >  <!--<h2 :class="counter>=0?'positive':'negative'">{{counter}}</h2>-->
    <h1>Hello</h1>
    <h2 :class="classCounter2()">{{counter}}</h2>
    <div class="btn-group">
      <button @click="incremento()" class="btn btn-success">Aumentar</button>
      <button @click="disminuirContador()" class="btn btn-danger">Disminuir</button>
      <button @click="resetear()" class="btn btn-secundary">resetear</button>
      <button :disabled="bloquear" @click="add()" class="btn btn-primary">Add</button>
      </div>  
    
    <ul class="list-group">
      <li class="list-group-item mt-4 border-0" v-for="num in arrayFavoritos"
      :key="index">
        {{num}}
      </li>
    </ul>
</div>

</template>

<style>
 h1{
  color:red
 }  
 .positive{
  color: green;
 }
 .negative{
  color: red;
 }
 .zero{
  color: peru;
 }
</style>