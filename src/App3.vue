<script setup>
  const objetofruta={
    name:"manzana",
    price:"1$",
    description:"una manzana",
    id:1
  }
  const arregloFrutas=[
        {
            name:"Manzana",
            price:"$1.00",
            description:"una manzana",
            stock:0
        },
        {
            name:"Pera",
            price:"$2.00",
            description:"una pera",
            stock:10
        },
        {
            name:"Naranja",
            price:"$3.00",
            description:"una naranja",       
            stock:30
        }
    ]

</script>

<template>
  <!--
  <ul>
    <li v-for="(value,propiedad,index) in objetofruta"
    :key="value"
    >
     {{propiedad}}:{{value}}:{{index}}
    </li>
  </ul>
  -->
  <ul>
    <template v-for="item in arregloFrutas" :key="item.name">

      <li v-if="item.stock>0">
     
         {{item.name}}-{{item.price}}
  
      </li>

    </template> 
  </ul>

</template>