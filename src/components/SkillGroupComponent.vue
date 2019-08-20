<template>
    <v-flex xs12 >
          <v-card-title>{{groupName}}:</v-card-title>
          <v-divider></v-divider>
          <skill-component
            v-for="skill in skills"
            :key="skill.name"
            :level="skill.level"
            :skill="skill.name"
            :barColor="colore"
          />
        </v-flex>
</template>

<script>
import SkillComponent from './SkillComponent.vue'
export default {
    name: 'SkillGroupComponent',
    components: {
        SkillComponent,
    },
    props: {
        skills: {
            required: true,
            type: Array
        },
        groupName: {
            type: String,
            required: true,
        },
        colore: {
            required: true
        },
    }
}
</script>