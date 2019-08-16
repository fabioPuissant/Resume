<template>
  <v-layout justify-space-around column>
    <v-flex></v-flex>
    <v-flex>
      <v-card color="deep-purple darken-1" class="pa-3">
        <v-row no-gutters>
          <v-col md="2" lg="2" sm="2">
            <v-list
              class="mx-auto hidden-sm-and-down"
              dark
              rounded
              text
              color="deep-purple darken-1"
            >
              <v-list-item-group color="deep-purple lighten-2">
                <v-list-item v-for="(item, i) in listItems" :key="i" @click="changeShow(item)">
                  <v-list-item-content>
                    <v-list-item-title>{{item}}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-col>
          <v-col align-self="center">
            <about v-if="show === 'about'" />
            <Skills v-if="show === 'skills'" />
          </v-col>
        </v-row>
      </v-card>
    </v-flex>
    <v-flex></v-flex>
  </v-layout>
</template>

<script>
import about from "../views/About.vue";
import Skills from "../views/Skills.vue";

export default {
  name: "DashboardMdScrnWidth",
  components: {
    about,
    Skills
  },
  data() {
    return {
      listItems: ["about", "internship", "skills", "goals", "international"],
      show: "about",
      drawer: false
    };
  },
  methods: {
    changeShow(prop) {
      this.show = prop;
    }
  },
  computed: {
    windowWidth() {
      return window.innerWidth;
    },
    align() {
      return this.windowWidth > 960 ? "align-start" : "align-end";
    }
  }
};
</script>