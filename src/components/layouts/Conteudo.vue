<template>

<div>
  <h1>Componente Conteudo</h1>
  <home></home>
  <publicar-vaga></publicar-vaga>
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
  } 

}

</script>

<style module>
h1 { 
  color: green;
}
</style>
