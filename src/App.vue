<template>
  <div>
    <h1>Componente App</h1>
    <topo-padrao /> 
    <conteudo></conteudo>
   </div>
</template>

<script>
//Oraganizar ordem alfabetica ou padrão
import Conteudo from './components/layouts/Conteudo.vue'
import TopoPadrao from './components/layouts/TopoPadrao.vue'



export default {
  name: 'App',
  components: {
    Conteudo: Conteudo,
    TopoPadrao: TopoPadrao, 
  }
}
</script>

<style>
h1 {
  color: blue;
}
</style>
