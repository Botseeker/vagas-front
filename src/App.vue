<template>
  <div>
    <vagas-favoritas></vagas-favoritas>
    <topo-padrao @navegar="componente = $event" /> 
    <conteudo v-if="visibilidade" :conteudo="componente"></conteudo>
   </div>
</template>

<script>
//Oraganizar ordem alfabetica ou padrão
import Conteudo from '@/components/layouts/Conteudo.vue'
import TopoPadrao from '@/components/layouts/TopoPadrao.vue'
import VagasFavoritas from './components/comuns/VagasFavoritas.vue'



export default {
  name: 'App',
  data: () => ({
    visibilidade: true,
    componente: 'Home'
  }),
  components: {
    Conteudo: Conteudo,
    TopoPadrao: TopoPadrao,
    VagasFavoritas
}
}
</script>

<style>

</style>
