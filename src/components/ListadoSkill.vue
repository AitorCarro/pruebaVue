<template>
<div class="container">
    <div class="card mt-3">
        <div class="card-body">
            <table class="table table-striped">
                <thead>
                    <tr>
                        <th scope="col">Soft skill</th>
                        <th scope="col">Valoracio</th>
                        <th></th>
                    </tr>

                </thead>
                <tbody id="table-body">
                    <!-- <SkillItem v-for="skillPrueba in skillsPruebas" v-bind:key="skillPrueba" :indice="skillPrueba['indice']" :skill="skillPrueba.skill" :num="skillPrueba.num"></SkillItem> -->
                    <SkillItem :indice=1 :habilidad=hhh :num=3></SkillItem>
                    <SkillItem :indice=2 :habilidad=hh1 :num=1></SkillItem>
                </tbody>
            </table>
        </div>
    </div>
</div>
</template>

<script>
import SkillItem from './SkillItem.vue'

export default {
  name: 'BtnAction',
  components: {
    SkillItem,
},
//   data: () => ({
//         skillsPruebas: [indice=> 1, skill => 'caca', num => '3'],
//   }),
}
</script>