<template>
    <tr>
        <td>{{ habilidad }}</td>
        <td>{{ num }}</td>
        <td>
            <!-- <button type="button" class="btn btn-danger" onclick="borrarValoracion(${i.indice})" id="${i.indice}">Esborrar</button> -->
        <BtnAction nombre="Esborrar" clase="btn btn-danger" v-bind:indice="i"/>
        </td>
    </tr>
</template>

<script>
import BtnAction from './BtnAction.vue'

export default {
  name: 'SkillItem',
  props: {  
    i: String,
    num: String,
    habilidad: String,
  },
  components: {
    BtnAction,
  }
}
</script>

