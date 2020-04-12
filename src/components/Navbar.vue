<template>
  
    <v-app-bar flat app  color="#1D1826">

      <v-toolbar-title class="white--text text-uppercase">
        <span>I-</span>
        <span class="font-weight-black">Talent</span>
      </v-toolbar-title>
      <v-spacer />
        <div>
        <v-btn v-for="(navItem, i) in navItems" :key="i" 
        text small color="error"
          router :to="navItem.to"
        >{{navItem.text}}</v-btn>
      </div>
    </v-app-bar>  
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      drawer: false,
      navItems: [
        { text: "Home", icon: "dashboard", to: "/" },
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
.bg-Skyline{
  background: url('/blury.jpg'), no-repeat, ;
}
.bg-color {
  background: #1D1826;
}
</style>