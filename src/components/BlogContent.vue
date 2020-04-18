<template>
<div   class="mx-auto pa-6">
<v-card :data-aos="fadeDirection"
    max-width="400">
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
              <v-chip small color="secondary" class="white--text">
                    {{article.category}}
                  </v-chip>
                  <v-spacer></v-spacer>
          <v-chip small replace color="info" v-bind:href="article.url" target="_blank">{{article.date}}</v-chip>
        </v-card-actions>
      </v-card>
</div>
    
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
AOS.init({
  duration: 1200
});

export default {
  props: {
    article: Object,
    fadeDirection: String
  }
};
</script>