
<template>
    <div class="container">
        <div class="card mt-3">
            <div class="card-body">
                <div class="row g-3">
                    <div class="col-md-8">
                        <SoftSkills titulo="Soft Skills"/>
                    </div>
                    <div class="col-md-4">
                        <label for="valoracio" class="form-label">Valoracio</label>
                        <input type="number" class="form-control" id="valoracio" min="0" max="3">
                    </div>
                    <div class="col-12">
                        <BtnAction nombre="Afegir" clase="btn btn-primary" id="btnAfegir"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import BtnAction from './BtnAction.vue'
import SoftSkills from './SoftSkills.vue'

export default {
  name: 'AnadirSkill',
  components: {
    BtnAction,
    SoftSkills,
  }
}
</script>


