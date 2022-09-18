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


</script>

<template>
  <!--<h2 :class="counter>=0?'positive':'negative'">{{counter}}</h2>-->
 <h2 :class="classCounter2()">{{counter}}</h2>
  <button @click="incremento()">Aumentar</button>
  <button @click="disminuirContador()">Disminuir</button>
  <button @click="resetear()">resetear</button>
  
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