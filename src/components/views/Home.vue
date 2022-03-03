<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <div class="h-100 p-5 bg-light border rounded-3 ">
          
          <h2>Pesquisar Vagas</h2>
          <div class="row">
            <div class="col">
              <div class="form-group">
                <label>Título da vaga</label>
                <input type="text" class="form-control" placeholder="Pesquisa palavra chave, ex: 'PHP', 'Pleno', 'Analista'">
                <small class="form-text text-muted">Informe palavras que estejam relacionadas com o título da vaga que você procura</small>      
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col">
              <button class="btn btn-outline-dark mt-2" type="button">Buscar</button>
            </div>
          </div>
        </div>

      </div>
    </div>

    <div class="row mt-5">
      <div class="col-4">
      </div>
    </div>
    
  </div>
</template>


<script>
export default {
  name: 'Home-',
  created() {
    console.log('Criado')
  },
  activated() {
    console.log('Activado')
  },
  deactivated() {
    console.log('desativado')
  },
  beforeUnmount() {
    console.log('Antes de desmontar')
  },
  unmounted() {
    console.log('Desmontar')
  },
}

</script>

<style module>

h1 {
  color: purple;

}

</style>
