<template>
  <v-container fill-height>
    <DashboardMdScrnWidth class="hidden-sm-and-down" />
    <DashboardSmScrnWidth class="hidden-md-and-up" />
  </v-container>
</template>

<script>
import DashboardMdScrnWidth from "../components/DashboardMdScrnWidth.vue";
import DashboardSmScrnWidth from "../components/DashboardSmScrnWidth.vue";
export default {
 components : {
   DashboardMdScrnWidth,
   DashboardSmScrnWidth
 }
};
</script>

<style scoped>

</style>