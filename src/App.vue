<template>
  <v-app class="grey lighten-4 ">
    <Navbar />
    <v-content class="bg-image-blured mt-4">
        <router-view id="view"/>
    </v-content>
      <v-footer class="secondary" app>
      <v-layout row wrap align-center>
        <v-flex xs12>
          <div class="white--text ml-3">
            Made with
            <v-icon class="red--text">favorite</v-icon>
            by <a class="white--text" href="https://vuetifyjs.com" target="_blank">Vuetify</a>
            and <a class="white--text" href="https://github.com/fabioPuissant" 
target="_blank">Fabio Puissant</a>
          </div>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  },
  data: () => ({
    //
  }),
};
</script>

<style scoped>
.bg-image-blured{
  background: no-repeat, center, 100%;
  background-size: cover;
  background-image: url('../public/bg2.jpg');
}

</style>
