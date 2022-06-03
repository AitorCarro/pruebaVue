<template>
    <button type="button" v-bind:class="clase" v-bind:id="indice" >
      {{ nombre }}
    </button>
</template>

<script>
export default {
  name: 'BtnAction',
  props: {
    clase: String,
    indice: String,
    nombre: String,
  }
}
</script>


