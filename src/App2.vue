<script setup>
    const hello="hello word"
    const arreglo=["uno","dos","tres"]
    const col=["red","blue"]
    const booleano=null
    const persona=[{
        nombre:"fernando",
        apellido:"barroso",
        edad:35
    },
    {
        nombre:"pamela ",
        apellido:"hidalgo",
        edad:37
    
    }
    
    
]
 const color="color:blue"
</script>
<template>
   <ul>
    <li 
         v-for="(nombre,index) in arreglo"
         :key="index"
             
        >
      {{nombre}}-{{index}}
    </li>
   </ul>

   <p v-if="booleano===true">este es booleano</p>
   <p v-else-if="booleano===false">no es es booleano</p>
   <p v-else>estoy indeciso</p>

   <ul>
     <li v-for="a in persona"
     :key="a.nombre"
      
     >
      {{a.nombre}}{{a.apellido}}
      {{a.edad}}    
    </li>
   </ul>

   <h2 :style="color">esto es un  color</h2>
   <h2 :style="`color:${col[0]}`">este es el color cero</h2>
</template>