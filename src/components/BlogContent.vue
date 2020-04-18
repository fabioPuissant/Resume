<template>
  <div class="mx-auto pa-6 hvr-float">
    <v-card
      v-on:hover=""
      :data-aos="fadeDirection"
      max-width="400"
      :class="{ 'on-hover': hover }"
    >
      <v-img height="300px" v-bind:src="article.urlToImage"></v-img>
      <v-container fill-height fluid>
        <v-layout>
          <v-flex xs12 align-end d-flex>
            <span class="headline">{{ article.title }}</span>
          </v-flex>
        </v-layout>
      </v-container>
      <v-card-text>{{ article.description }}</v-card-text>
      <v-card-actions>
        <v-chip small color="secondary" class="white--text">{{article.category}}</v-chip>
        <v-spacer v-if="article.hasOwnProperty('link')"></v-spacer>
        <v-btn
          v-if="article.hasOwnProperty('link')"
          icon
          class="red--text"
          v-on:click="redirectTo(article.link)"
        >
          <v-icon large>{{article.icon}}</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-chip
          small
          replace
          color="info"
          v-bind:href="article.url"
          target="_blank"
        >{{article.date}}</v-chip>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init({
  duration: 1000
});

export default {
  data() {
    return {
      "hover": false,

    }
  },
  props: {
    article: Object,
    fadeDirection: String,
  },
  methods: {
    redirectTo(location) {
      window.location.replace(location);
    }
  }
};
</script>

<style scoped>


.v-card:not(.on-hover) {
  opacity: 0.6;
}

.show-btns {
  color: rgba(255, 255, 255, 1);
}
</style>