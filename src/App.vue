<template>
  <v-app class="grey lighten-4 ">
    <Navbar />
    <v-content class="bg-color-dark mt-4">
        <router-view id="view"/>
    </v-content>
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

.bg-color-dark {
  background-color: #1D1826;
}

</style>
