<template>
  <div :class="'h-100 p-5 rouded-3 border ${bg} ${color}'">
    <p>{{ titulo }}</p>
    <h2>{{ indicador }}</h2>
  </div>
</template>

<script>
export default {
    name: 'Indicador-',
    props: ['titulo', 'indicador', 'bg', 'color']
}
</script>

<style>
</style>