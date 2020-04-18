<template>
   <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-row 
        wrap
        align="start"
          justify="center"
          >
      <BlogContent v-for="(article, i) in articles" :key="i"
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
import BlogContent from '../components/BlogContent'
export default {
  name: "Blog",
  components: {
    BlogContent
  },
  data() {
    return {
      start: true,
      subject: "",
        articles: require('@/data/articles.json'),
    };
  },
  methods: {
    choseBlogSubject(prop) {
      this.start = !this.start;
      this.subject = prop;
    },
  },
};
</script>

<style scoped>

</style>

