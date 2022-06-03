<template>
<AnadirSkill/>
<ListadoSkill/>
</template>

<script>
import AnadirSkill from './components/AnadirSkill.vue'
import ListadoSkill from './components/ListadoSkill.vue'

export default {
  name: 'App',
  components: {
    AnadirSkill,
    ListadoSkill
  }
}
</script>
