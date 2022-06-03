<template>
    <label for="softSkill" class="form-label"> {{ titulo }}</label>
        <select name="softSkill" id="softSkill" class="form-select">
            <option v-for="skill in skills" v-bind:key="skill">{{skill}}</option>
        </select>
</template>

<script>
export default {
  name: 'SoftSkills',
  props: {
    titulo: String,
  },
  data: () => ({
    skills: ["Flexibilitat", "Responsabilitat", "Autonomia", "Sociabilitat", "Evolució"],
}),
}
</script>
