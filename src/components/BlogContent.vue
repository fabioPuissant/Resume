<template>
    <v-flex lg10 md10>
      <v-card class="my-3" :data-aos="fadeDirection">
        <v-img height="350px" v-bind:src="article.urlToImage"></v-img>
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
                    {{article.source.name}}
                  </v-chip>
                  <v-spacer></v-spacer>
          <v-btn small replace color="info" v-bind:href="article.url" target="_blank">Read More</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
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