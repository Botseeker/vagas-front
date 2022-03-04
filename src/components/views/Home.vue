<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <pesquisar-vaga></pesquisar-vaga>
      </div>
    </div>
    <div>
      <div class="row mt-5">
        <div class="col-4">
          <indicador titulo="Vagas abertas" indicador="100"
           bg="bg-dark" color="text-white"></indicador>
        </div>
      </div>

      <div class="col-4">
        <indicador titulo="Profissionais cadastrados" indicador="225"
         bg="bg-dark" color="text-white"></indicador>
      </div>

      <div class="col-4">
        <indicador titulo="Visitantes online" indicador="25"
         bg="bg-dark" color="text-white"></indicador>
      </div>
    </div>
  </div>
</template>


<script>
import PesquisarVaga from '@/components/comuns/PesquisarVaga.vue'
import Indicador from '@/components/comuns/Indicador.vue'


export default {
  
  name: "Home-",
  components: {
    PesquisarVaga,
    Indicador
  },
  created() {
    console.log('Criado', this.teste);
  },
  activated() {
    console.log("Activado");
  },
  deactivated() {
    console.log("desativado");
  },
  beforeUnmount() {
    console.log("Antes de desmontar");
  },
  unmounted() {
    console.log("Desmontar");
  },
};
</script>

<style module>
h1 {
  color: purple;
}
</style>
