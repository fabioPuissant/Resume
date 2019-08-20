<template>
  <nav>
    <v-app-bar flat app color="teal">
      <v-app-bar-nav-icon color="white" @click="showNav"></v-app-bar-nav-icon>

      <v-toolbar-title class="white--text text-uppercase">
        <span>I-</span>
        <span class="font-weight-black">Talent</span>
      </v-toolbar-title>
    </v-app-bar>
    <v-navigation-drawer color="cyan darken-3" dark v-model="drawer" app>
        <v-row justify-sm="end" class="pr-5 pt-3">
          <v-spacer></v-spacer>
        <v-icon right color="white" @click="showNav">clear</v-icon>
           </v-row>
      <v-layout column align-center>
        <v-flex mt-5>
          <v-avatar size="100">
            <img src="/avatar-6.JPG" />
          </v-avatar>
        </v-flex>
        <v-flex mt-5>
          <span class="white--text font-weight-bold">Fabio Puissant</span>
          <v-divider></v-divider>
        </v-flex>
      </v-layout>
      <v-list mt-5>
        <v-list-item-group>
          <v-list-item
            v-for="(navItem,i) in navItems"
            :key="i"
            justify-center
            router
            :to="navItem.to"
            
          >
            <v-list-item-content>{{navItem.text}}</v-list-item-content>
            <v-list-item-icon>
              <v-icon>{{navItem.icon}}</v-icon>
            </v-list-item-icon>
          </v-list-item>
          <v-divider dark></v-divider>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      drawer: false,
      navItems: [
        { text: "Dashboard", icon: "dashboard", to: "/" },
        { text: "Blog", icon: "people", to: "/blog" },
        { text: "Contact", icon: "alternate_email", to: "/contact" }
      ],
      crossShow: true,
      menuShow: true
    };
  },
  methods: {
    showNav() {
      this.drawer = !this.drawer;
    }
  }
};
</script>

<style scoped>
</style>