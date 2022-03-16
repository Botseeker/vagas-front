<template>
    <div>
        <div :class="estiloAlerta" role="alert">
            <slot name="titulo">
                <h3>Título msg feedback</h3>
            </slot>
            <hr>
            <slot><p>Msg de feedback</p></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Alerta-',
    props: { tipo: String },
   computed: {
       estiloAlerta() {
           switch(this.tipo) {
               case 'erro': return 'alert alert-danger'
               case 'success': return 'alert alert-success'
               default: return 'alert alert-success'
           }
       }
   }
}
</script>

<style>

</style>