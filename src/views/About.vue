<template>
  <v-card light class="mx-auto" height="100%" width="100%">
    <v-card-title v-if="smallScrn">About</v-card-title>

    <v-card-title class="fill-height align-end">
      <v-layout column align-center>
        <v-flex>
          <v-avatar size="100" class="mb-3">
            <v-img src="/avatar-6.JPG"></v-img>
          </v-avatar>
        </v-flex>
        <v-flex>
          <v-row class="mb-1" justify-sm="center">
            <span class="font-weight-light">Hi, I'm &nbsp;</span>
            <span
              class="font-weight-bold teal--text text-capitalize lighten-2"
            >Fabio puissant</span>
          </v-row>
          <v-row justify-sm="center">
             <span
              class="font-weight-bold caption teal--text text-capitalize lighten-3"
            >UI</span>
            <span class="caption">,</span>
            <span
              class="font-weight-bold caption teal--text text-capitalize lighten-3"
            > &nbsp;Web</span>
            <span class="caption">,</span>            
            <span
              class="font-weight-bold caption teal--text text-capitalize lighten-3"
            > &nbsp;Fullstack &nbsp;</span>
            <span class="font-weight-light caption">Freelancer</span>
          </v-row>
          <v-row>
            <v-divider></v-divider>
          </v-row>
          <v-row class="my-2"></v-row>
          <v-row justify-sm="center">
            <div class="caption font-weight-light">
              Professional&nbsp;
              <span class="font-weight-bold teal--text darken-2">Web&nbsp;</span>
              <span>and&nbsp;</span>
              <span class="font-weight-bold teal--text darken-2">Android&nbsp;</span>
             <span>Development,&nbsp;</span>
              <span class="font-weight-bold teal--text darken-2">Backend&nbsp;</span>
              Solutions
            </div>
          </v-row>
          <v-row>
            Full stack developer with passion for tech.
          </v-row>
        </v-flex>
      </v-layout>
    </v-card-title>
    <v-card-text>
      <v-row>
        <v-col
          cols="10">
          I have worked in different sectors for three years, before I find my passion and started my studies in informatics.
          My experience as a call agent agent boosted my social skills. After this job I worked as an electrician in a big company.
          There I was promoted as a team leader after 1 year. Still I wasn't satisfied. I always wanted a job in technology. So one year later, at the age of 23, 
          I decided to start my studies at Hogeschool PXL Hasselt to get my bachelor degree in applied informatics.
          <br> I am very passionate about my studies. In the future I aim to travel the world so I can learn new concepts and technologies to expand my horizon.
          <br> The main goal for me is to learn as much as I can possible can and be the best version of myself.
        </v-col>
        <v-col cols="2">
          <v-responsive>
            <v-img max-height="100" max-width="300" src="/avatar-6.JPG"></v-img>
          </v-responsive>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "about",
  props: {
    smallScrn: {
      required: false,
    }
  }
};
</script>

<style scoped>
</style>