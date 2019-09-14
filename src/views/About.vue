<template>
  <v-card light class="mx-auto" height="100%" width="100%">
    <v-card-title v-if="smallScrn" class="grey--text">About</v-card-title>

    <v-card-title class="fill-height align-end">
      <v-layout column align-center>
        <v-flex>
          <v-avatar class="profile mb-sm-3" size="100" tile>
            <v-img src="/fabio.png"></v-img>
          </v-avatar>
        </v-flex>
        <v-flex>
          <v-row class="text-center" justify-sm="center">
            <v-col>
              <span class="font-weight-light">Hi, I'm &nbsp;</span>
              <span class="font-weight-bold teal--text text-capitalize lighten-2">Fabio puissant</span>
            </v-col>
          </v-row>
          <v-row >
            <v-col class="text-center my-0">
              <span class="font-weight-bold caption teal--text text-capitalize lighten-3">UI</span>
              <span class="caption">,</span>
              <span class="font-weight-bold caption teal--text text-capitalize lighten-3">&nbsp;Web</span>
              <span class="caption">,</span>
              <span
                class="font-weight-bold caption teal--text text-capitalize lighten-3"
              >&nbsp;Fullstack &nbsp;</span>
              <v-divider class="mx-5"></v-divider>
            </v-col>
          </v-row>
          <v-row justify-sm="center">
            <v-col :class="['caption my-0 text-center font-weight-light', $vuetify.breakpoint.mdAndDown ? 'caption' : 'subheader']">
              <span>Professional&nbsp;</span> 
              <span :class="['font-weight-bold teal--text darken-2',]">Web&nbsp;</span>
              <span>and&nbsp;</span>
              <span class="font-weight-bold teal--text darken-2">Android&nbsp;</span>
              <span>Development,&nbsp;</span>
              <span class="font-weight-bold teal--text darken-2 line">Backend&nbsp;</span>
              <span class="line">Solutions</span>
            </v-col>
          </v-row>
          <v-row>
            <v-col align="center" :class="['ma-0 text-center', $vuetify.breakpoint.smAndDown ? 'heading' : '' ]">
            Full stack developer with passion for tech.
            </v-col>
            </v-row>
        </v-flex>
      </v-layout>
    </v-card-title>
    <v-card-text>
      <v-row class="text-center caption">
        <v-col>
          <div class="title text-left ma-0 teal--text text--darken-1">Background:</div>
          <br />I worked in different sectors for three years, before I found my passion and started my studies in computer science. My experience as a call agent agent boosted my social skills. After this job, I worked as an electrician in a big company. There I was promoted as a team leader after 1 year. Still I wasn't satisfied. I always wanted a job in technology. So one year later, at the age of 23, I decided to start my studies at Hogeschool PXL Hasselt to get my bachelor's degree in Computer Science. I am very passionate about my studies. I aim to travel the world so I can learn new concepts and technologies.
          My main goal is to learn as much as I can so I can travel the world, doing what I love.
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
      required: false
    }
  }
};
</script>

<style scoped>
span{
  display: inline-block;
}
</style>