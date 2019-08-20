<template>
  <v-card style="max-height: 400px" class="overflow-y-auto" color="grey--text">
    <v-container>
      <v-layout wrap justify-start>
        <SkillGroupComponent
          v-for="sg in skillsGroups"
          :key="sg.groupName"
          :colore="sg.barColor"
          :groupName="sg.groupName"
          :skills="sg.skills"
          class="mb-3"
        />
      </v-layout>
    </v-container>
  </v-card>
</template>

<script>
import SkillGroupComponent from "../components/SkillGroupComponent.vue";
export default {
  name: "Skills",
  components: {
    SkillGroupComponent
  },
  data() {
    return {
      skillsGroups: [
        {
          groupName: "Code",
          barColor: "cyan lighten-2",
          skills: [
            { name: "Java", level: 80 },
            { name: "C#", level: 83 },
            { name: "ASP.NET", level: 85 },
            { name: "PHP", level: 70 },
            { name: "Vue JS", level: 78 }
          ]
        },
        {
          groupName: "Professional skills",
          barColor: "deep-purple lighten-2",
          skills: [
            { name: "Communication", level: 80 },
            { name: "Confidence", level: 83 },
            { name: "Leadership", level: 85 }
          ]
        }
      ]
    };
  }
};
</script>

<style scoped>
</style>