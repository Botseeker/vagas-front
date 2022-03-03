<template>

<div>
  <h1>{{ titulo }}</h1>
  <button @click="atualizar()">Atualizar</button>
  <button @click="conteudo = 'home'">Home</button>
  <button @click="conteudo = 'publicar-vaga'">Publicar Vaga</button>
  <!-- renderizar de modo dinâmico os componentes home e publicar -->
  <!--<home></home>
  <publicar-vaga></publicar-vaga> -->
  <keep-alive>
    <component :is="conteudo" />
  </keep-alive>
</div>
</template>


<script>
import Home from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVagas.vue'
export default {
  name: 'Conteudo-',
  components: {
    Home,
    PublicarVaga
  },
  data: () => ({
    teste: 'O componente foi criado',
    titulo: 'Componente conteudo',
    conteudo: 'home'

  }),
  methods: {
    atualizar() {
      this.titulo += '*'
    }
  },
  /*
  // Lifecycle_Hooks
  beforeCreate() {
    console.log('Antes de criar', this.teste)
  },
  created() {
    console.log('Criado')
  },
  beforeMount() {
    console.log('Antes de montar o template')
  },
  mounted() {
    console.log('montado')
  },
  beforeUpdate() {
    console.log('Antes de atualizar')
  },
  update() {
    console.log('atualizar')
  },
   
  
  errorCaptured() {
    console.log
  },
  erroTracked () {
    console.log('Erro de monitoramento')
  },
  randerTracked() {
    console.log('Re-renderização rastrada')
  },
  renderTriggered() {
    console.log('Re-renderização ativada')
  },
  activated() {
    console.log('Activado')
  },
  deactivated() {
    console.log('desativado')
  }
  */
}

</script>

<style module>
h1 { 
  color: green;
}
</style>
