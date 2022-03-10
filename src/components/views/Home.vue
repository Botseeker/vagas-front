<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <pesquisar-vaga></pesquisar-vaga>
      </div>
    </div>
    

    <div class="row mt-5" v-for="(vaga, index) in vagas" :key="index">
      <div class="col">
        <vaga v-bind="vaga"  /> 
      </div>
    </div> 

      <div>
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
      <div></div>
    </div>
  </div>
</template>


<script>
import PesquisarVaga from "@/components/comuns/PesquisarVaga.vue";
import Indicador from "@/components/comuns/Indicador.vue";import Vaga from "@/components/comuns/Vaga.vue";

export default {
  name: "Home-",
  components: {
    PesquisarVaga,
    Indicador,
    Vaga
  },
  data: () => ({
      usuariosOnline: 0,
      vagas: []
  }),
  methods: {
    getUsuariOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101)
    }
  },
  created() {
    setInterval(this.getUsuariOnline, 60000)
  },
  activated() { //
    this.vagas = JSON.parse(localStorage.getItem('vagas'))

  }
}
</script>

<style>

</style>
