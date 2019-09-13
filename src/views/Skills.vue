<template>
  <v-card style="max-height: 600px" class="overflow-y-auto" color="grey--text">
    <v-card-title v-if="smallScrn">Skills</v-card-title>
    <v-container>
      <v-layout wrap justify-start class="px-3">
        <SkillGroupComponent
          v-for="sg in skillsGroups"
          :key="sg.groupName"
          :colore="sg.barColor"
          :groupName="sg.groupName"
          :skills="sg.skills"
          :icon="sg.icon"
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
          icon: 'code',
          skills: [
            { name: "Java", level: 80 },
            { name: "C#", level: 83 },
            { name: "ASP.NET", level: 85 },
            { name: "PHP", level: 70 },
            { name: "Vue JS", level: 78 },
            { name: "Flutter", level: 60 },
          ]
        },
        {
          groupName: "Professional skills",
          barColor: "deep-purple lighten-2",
          icon: 'people',
          skills: [
            { name: "Communication", level: 90 },
            { name: "Confidence", level: 83 },
            { name: "Leadership", level: 85 }
          ]
        }
      ]
    };
  },
  props: {
    smallScrn: {
      required: false
    }
  }
};
</script>

<style scoped>
</style>