<template>

<div>
  <keep-alive>
    <component :is="conteudo" />
  </keep-alive>
</div>

</template>


<script>
import Home from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVagas.vue'
export default {
  props: {
    conteudo: {
      type: String,
      required: true
    }
  },
    name: 'Conteudo-',
    components: {
    Home,
    PublicarVaga
  },
}

</script>

<style module>

</style>
