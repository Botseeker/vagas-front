<template>
  <div>
    
    <vagas-favoritas></vagas-favoritas>
    <topo-padrao @navegar="componente = $event" /> 
    <alerta v-if="exibirAlerta">
      <template v-slot:titulo>
        <h5>Título do Alerta</h5>
      </template>

      <template v-slot:descricao>
        <p>Descrição do Alerta</p>
      </template>
    </alerta>
    <conteudo v-if="visibilidade" :conteudo="componente"></conteudo>
   </div>
</template>
<!-- <div class="alert alert-success" role="alert">
        <h5>Título Alerta</h5>
        <hr>
        <p>Vaga Cadastrada Com Sucesso!</p>
      </div> -->
<script>
//Oraganizar ordem alfabetica ou padrão
import Alerta from '@/components/comuns/Alerta.vue'
import Conteudo from '@/components/layouts/Conteudo.vue'
import TopoPadrao from '@/components/layouts/TopoPadrao.vue'
import VagasFavoritas from './components/comuns/VagasFavoritas.vue'



export default {
  name: 'App',
  data: () => ({
    visibilidade: true,
    componente: 'Home',
    exibirAlerta: false
  }),
  components: {
    Alerta,
    Conteudo,
    TopoPadrao,
    VagasFavoritas
  },
  mounted() {
    this.emitter.on('alerta', () => {
      this.exibirAlerta = true
      setTimeout(() => this.exibirAlerta = false, 5000)
      console.log('Apresentar Alerta Customizado')
    })
  }
}
</script>

<style>

</style>
