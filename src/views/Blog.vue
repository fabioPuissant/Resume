<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <v-row>
          <v-tabs background-color="transparent" centered dark icons-and-text>
            <v-tabs-slider></v-tabs-slider>

            <v-tab v-on:click="choseBlogSubject('Seminar')">Seminar</v-tab>

            <v-tab v-on:click="choseBlogSubject('International')">International</v-tab>

            <v-tab v-on:click="choseBlogSubject('Event')">Event</v-tab>
          </v-tabs>
        </v-row>
      </v-col>
      <v-col cols="12">
        <v-row wrap align="start" justify="center">
          <BlogContent
            v-for="(article, i) in rightArticles"
            :key="i"
            :article="article"
            :fadeDirection=" i%2 == 0 ? 'fade-right' : 'fade-left'"
            class="mx-auto mt-8"
          ></BlogContent>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import BlogContent from "../components/BlogContent";
export default {
  name: "Blog",
  components: {
    BlogContent
  },
  data() {
    return {
      start: true,
      subject: "Seminar",
      articles: require("@/data/articles.json")
    };
  },
  methods: {
    choseBlogSubject(prop) {
      this.subject = prop;
    },
    printSome(val) {
      console.log(`${val}`);
    }
  },
  computed: {
    rightArticles: function() {
      console.log(this.chosenArticleType);
      return this.articles.filter(t => t.category === this.subject);
    }
  }
};
</script>

<style scoped>
</style>

