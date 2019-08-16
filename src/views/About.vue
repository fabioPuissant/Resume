<template>
  <v-card light class="mx-auto" height="100%" width="100%">
    <v-card-title class="fill-height align-end">
      <v-layout column align-center>
        <v-flex>
          <v-avatar class="mb-3">
            <v-img src="/avatar-6.JPG"></v-img>
          </v-avatar>
        </v-flex>
        <v-flex>
          <v-row class="mb-1">
            <span class="font-weight-light">Hi, I'm &nbsp;</span>
            <span
              class="font-weight-bold deep-purple--text text-capitalize lighten-2"
            >Fabio puissant</span>
          </v-row>
          <v-row justify-sm="center">
            <span class="font-weight-bold caption deep-purple--text text-capitalize lighten-2">Web, &nbsp;</span>
            <span class="font-weight-bold caption deep-purple--text text-capitalize lighten-2" >Fullstack, &nbsp;</span>
            <span class="font-weight-bold caption deep-purple--text text-capitalize lighten-2">UI &nbsp;</span>
            <span class="font-weight-light caption"> Development</span>
            
          </v-row>
          <v-row>
            <v-divider></v-divider>
          </v-row>
        </v-flex>
      </v-layout>
    </v-card-title>

    <v-card-text>
      <v-row>
        <v-col
          cols="10"
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Animi ipsam nostrum velit adipisci cumque nulla hic aspernatur suscipit ipsa, ex sit amet! Earum possimus est nobis laudantium repellendus architecto ratione.</v-col>
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
  name: "about"
};
</script>

<style scoped>
</style>