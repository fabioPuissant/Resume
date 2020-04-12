<template>
  <v-layout justify-space-around column>
    <v-flex>
    
        <v-row no-gutters>
          <v-col cols="2">
            <v-list
              class="mx-auto hidden-sm-and-down transparant-bg"
              tile
              text
              dark
              color="white--text"
            >
              <v-list-item-group>
                <v-list-item v-for="(item, i) in listItems" :key="i" @click="changeShow(item.text)">
                  <v-list-item-icon class="mr-3">
                    <v-icon left size="20">{{item.icon}}</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title class="text-capitalize caption">{{item.text}}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list-item-group>
            </v-list>
          </v-col>
          <v-col align-self="center">
            <about v-if="show === 'about'" />
            <Skills v-if="show === 'skills'" />
            <experience v-if="show === 'experience'" />
          </v-col>
        </v-row>
    </v-flex>
    <v-flex></v-flex>
  </v-layout>
</template>

<script>
import about from "../views/About.vue";
import Skills from "../views/Skills.vue";
import Experience from "../views/Experience.vue";

export default {
  name: "DashboardMdScrnWidth",
  components: {
    about,
    Skills,
    Experience,
  },
  data() {
    return {
      listItems: [
        { text: "about", icon: "fingerprint" },
        { text: "skills", icon: "code" },
        { text: "experience", icon: "work" },
      ],
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
<style scoped>
.gradient {
    background-image: linear-gradient(
    #ff5248,  #40212d
    ) !important;
    
}
.transparant-bg {
  background-color: transparent !important;
}
</style>