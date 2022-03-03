<template>
  <div>
    <h1>Componente App</h1>
    <button @click="desmontarComponente()">Desmontar_componente_conteúdo</button>
    <topo-padrao /> 
    <conteudo v-if="visibilidade"></conteudo>
   </div>
</template>

<script>
//Oraganizar ordem alfabetica ou padrão
import Conteudo from '@/components/layouts/Conteudo.vue'
import TopoPadrao from '@/components/layouts/TopoPadrao.vue'



export default {
  name: 'App',
  data: () => ({
    visibilidade: true
  }),
  methods: {
    desmontarComponente(){
      this.visibilidade = false
    }
  },
  components: {
    Conteudo: Conteudo,
    TopoPadrao: TopoPadrao, 
  }
}
</script>

<style>

</style>
