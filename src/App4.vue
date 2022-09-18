<script setup>
//metodo
const handleClick=(message)=>{
  console.log(message)

}
</script>

<template>
  <!--
  <button v-on:click="handleClick('texto1')">Activame</button>
  <button @click="handleClick('texto2')">Activame</button>
  <button @click="handleClick('texto2')">Activame</button>
  -->
  <button @click.right.prevent="handleClick('texto right')">Activame right</button>
  <button @click.left.prevent="handleClick('texto2 left')">Activame left</button>
  <button @click.middle.prevent="handleClick('texto2 middle')">Activame middle</button>
</template>