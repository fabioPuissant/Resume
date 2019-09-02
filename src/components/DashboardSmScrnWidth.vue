<template>
  <div>
    <v-col>
      <about smallScrn="true" />
    </v-col>
    <v-col>
      <skills smallScrn="true" />
    </v-col>
     <v-col>
      <experience smallScrn="true" />
    </v-col>
  </div>
</template>

<script>
import about from "../views/About.vue";
import Skills from "../views/Skills.vue";
import Experience from "../views/Experience.vue"

export default {
  name: "DashboardSmScrnWidth",
  components: {
    about,
    Skills,
    Experience,
  }
};
</script>