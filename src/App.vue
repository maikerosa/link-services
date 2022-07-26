<script setup>
import Item from "./components/item.vue"
</script>

<script>
import Dados from './Dados/Services.json'
export default {
  data(){
    return {
      servicos: null
      
    }
  },
  mounted(){
    this.servicos = Dados

  }
}
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>

   <h1>Seja bem-vindo(a)</h1>
   <hr/>
   <div class="itens">
    <Item 
      v-for="servico, index in servicos"
      :key="index"
      :item="servico"
    />
   </div>

  
   
</template>

<style> /** scoped só servirá para esse arq */
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

html{
  background: url("https://i.ibb.co/ygPr07R/Design-sem-nome.png");
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 100%;

}

.itens{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>

<style scoped>
img{
  width: 70px;
}
</style>