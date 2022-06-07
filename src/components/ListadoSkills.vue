<template>
<div class="container">
    <div class="card mt-3">
        <div class="card-body">
            <div class="row g-3">
                <div class="col-md-8">
                    <label for="softSkill" class="form-label">Soft Skills</label>
                        <select name="softSkill" id="softSkill" v-model= "softSkill" class="form-select">
                            <option v-for="softSkill in softSkills" v-bind:key="softSkill" >{{ softSkill }}</option>
                        </select>
                </div>
                <div class="col-md-4">
                    <label for="valoracio" class="form-label">Valoracio</label>
                    <input type="number" class="form-control" v-model= "valoracio" id="valoracio" min="0" max="3" @focusout="update()">
                </div>
                <div class="col-12">
                    <button type="button" class="btn btn-primary" id="btnAfegir" @click="addRow()">
                        Afegir
                    </button>
                </div>
            </div>
        </div>
    </div>

    <div class="card mt-3">
        <div class="card-body">
            <table class="table table-striped">
                <thead>
                    <tr>
                        <th scope="col">Soft skill</th>
                        <th scope="col">Valoracio</th>
                        <th scope="col">Acció</th>
                    </tr>
                </thead>
                <tbody id="table-body" v-for="row, index in rows" v-bind:key="row" >
                    <tr>
                        <td>{{ row.skillName }}</td>
                        <td>{{ row.num }}</td>
                        <td>
                            <button type="button" class="btn btn-danger" v-on:click="removeRow(index)" v-bind:id="index">Esborrar</button>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</div>
</template>

<script>

export default {
  name: 'ListadoSkillS',
  data: () => ({
    rows: [],
    softSkill: 'Flexibilitat',
    softSkills: ['Flexibilitat', 'Responsabilitat', 'Autonomia', 'Sociabilitat', 'Evolució'],
  }),
  methods: {
    update() {
        if (this.valoracio > 3 || this.valoracio < 0) {
            alert('Introdueix un valor entre 0 i 3.');
        }
    },
    addRow() {
        this.rows.push({skillName: this.softSkill , num: this.valoracio});
    },
    removeRow(index) {
        this.rows.splice(index, 1);
    }
  }
}
</script>