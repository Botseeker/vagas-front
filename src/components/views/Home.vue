<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <pesquisar-vaga></pesquisar-vaga>
      </div>
    </div>


    <lista-vagas>

      <!-- <template v-slot:titulo="slotProps">
        {{slotProps.dadosTitulo.titulo}}
        <hr>
      </template>
      
      <template v-slot:default="slotProps">
        {{slotProps.vagas}}
        <hr>
      </template>
      
      <template v-slot:rodape="slotProps">
        {{slotProps.dadosRodape.titulo}}
      </template> -->
    
    </lista-vagas>
    

    <div class="container py-4">
      <div class="row">
        <div class="col">
          <indicador
            titulo="Vagas disponíveis"
            indicador="150"
            bg="bg-dark"
            color="text-light">
          </indicador>
        </div>

        <div class="col">
          <indicador
            titulo="Profissionais cadastrados"
            indicador="225"
            bg="bg-light"
            color="text-dark">
          </indicador>
        </div>

        <div class="col">
          <indicador
            titulo="Visitantes Online"
            :indicador="usuariosOnline"
            bg="bg-dark"
            color="text-light">
          </indicador>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import PesquisarVaga from "@/components/comuns/PesquisarVaga.vue";
import Indicador from "@/components/comuns/Indicador.vue";
import ListaVagas from "@/components/comuns/ListaVagas.vue";

export default {
  name: "Home-",
  components: {
    PesquisarVaga,
    Indicador,
    ListaVagas,
  },
  data: () => ({
    usuariosOnline: 0,
  }),
  methods: {
    getUsuariOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101);
    },
  },
  created() {
    setInterval(this.getUsuariOnline, 60000);
  },
};
</script>

<style>
</style>
