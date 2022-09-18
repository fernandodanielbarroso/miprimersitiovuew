<script setup>
    const name="Vue Dinámico"
    const styleColor="color:blue"
    const arrayColores=["blue","red","peru"]
    const activo=false
    const arrayfrutas=["manzana","pera","tomate"]
    const arregloFrutas=[
        {
            name:"Manzana",
            price:"$1.00",
            description:"una manzana",
            id:1
        },
        {
            name:"Pera",
            price:"$2.00",
            description:"una pera",
            id:2
        },
        {
            name:"Naranja",
            price:"$3.00",
            description:"una naranja",       
            id:3
        }
    ]

</script>
<template>
  
    <h1>Hello {{name.toUpperCase()}}</h1>
    <!--<h2 v-bind:style="styleColor">Soy Azul</h2>-->
    <!--<h2>{{arrayColores}}</h2>-->
    
    <!--<h2 :style="`color:${arrayColores[2]}`">soy Perú</h2>
    <h2>
        {{
            activo?'estoy activo':'estoy inactivo'
        }}
    </h2>
    <p v-if="activo===true">
      <span>incono</span>
      Estoy activo
    </p>
    <p v-else-if="activo===false">estoy inactivo</p>
    <p v-else>estoy indeciso</p>

    <h2 v-show="activo">estoy activo v-show</h2>
    <ul>
        <li 
           v-for="(fruta,index) in arrayfrutas"
           :key="index"
             
        >
        {{index }}{{fruta}}


        </li>
    </ul>
-->
<ul>
    <li
     v-for="fruta in arregloFrutas"
     :key="fruta.id" 
    >
    {{fruta.name}}-{{fruta.id}}-{{fruta.price}}-{{fruta.description}}
  </li>
</ul>
    
</template>

<style>
    h1{
        color: red;
    }
</style>