<template>
  <v-card style="max-height: 600px" class="overflow-y-auto">
    <v-card-title v-if="smallScrn" class="grey--text">Experience</v-card-title>
    <v-timeline  class="my-1">
      <v-timeline-item v-for="(year, i) in years" :key="i" color="cyan lighten-2" large>
        <template v-slot:icon>
          <v-avatar>
            <img :src="year.avatar" />
          </v-avatar>
        </template>
        <template v-slot:opposite>
          <span>{{year.year}}</span>
        </template>
        <v-card class="elevation-1 mx-1" color="cyan lighten-4">
          <v-card-title>{{year.company}}</v-card-title>
          <v-card-text
            class="caption"
          >{{year.function}}</v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-card>
</template>

<script>
export default {
  name: "Experience",
  data () {
      return {
          years: [
              {year: 2015, avatar: '/ipg.jpg', function: 'Sales: Call agent', company: 'IPG - Hasselt'},
              {year: 2016, avatar: '/demtec.jpeg', function: 'Electrician: Maintenance', company: 'Demtec Services - Hasselt'},
              {year: 2017, avatar: '/pxl.png', function: 'Start studies: Applied informatics', company: 'Hogeschool PXL - Hasselt'},
              {year: 2019, avatar: '/android.png', function: 'Location based Android application', company: 'BUS-IT week: Brno - Czech Republic'},
              {year: 2020, avatar: '/belgiumCampus.png', function: 'Internship', company: 'Belgium Campus: Pretoria - South-Africa'},
              {year: 2020, avatar: '/pxl.png', function: 'Bachelor degree', company: 'Hogeschool PXL - Hasselt'},
          ]
      }
  },
  methods: {
       sort() {
      this.years.sort((a, b) => (a['year'] < b['year'] ? 1 : -1));
    }
  },
  created() {
      this.sort();
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