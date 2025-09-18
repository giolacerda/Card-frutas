<script lang="ts">
 export default{
    props: {
        infoFrutas:{
            type: Object,
            required: true
        }
    }
 }
</script>

<template>
    <div class="card">
        <p>{{ infoFrutas.nome }}</p>
        <p>{{ infoFrutas.cor }}</p>
    </div>
</template>

<style scoped>
.card {
  width: 150px;               /* largura pequena */
  padding: 1rem;
  margin: 0.5rem;
  border-radius: 10px;
  color: #fff;
  font-weight: bold;
  text-align: center;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: var(--cor-fruta, #888); /* cor padrão caso a prop não defina */
}

/* Efeito hover */
.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 15px rgba(0,0,0,0.2);
}

/* Container no App.vue para dispor os cards em colunas */
.corpo-app{
    display: flex;
flex-wrap: wrap;
gap: 1rem;
justify-content: center;
}
</style>
