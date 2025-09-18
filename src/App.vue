<script lang="ts">
import FrutasCard from './components/FrutasCard.vue';

export default{
 data() {
  return{
    frutas: [
      {nome: "Banana", cor: "Amarela"},
      {nome: "Maça", cor: "Vermelha"},
      {nome: "Laranja", cor: "Laranja"},
      {nome: "Morango", cor: "Vermelho"},
      {nome: "Pitaia", cor: "Rosa"},
      {nome: "Melancia", cor: "Verde"}
    ]
  }
 },
 components: {FrutasCard}
}
</script>

<template>
 <div class="corpo-app">
  <FrutasCard v-for="(infoFrutas,index) in frutas"
  :key="index"
  :info-frutas="infoFrutas"
  />

 </div>
 </template>
