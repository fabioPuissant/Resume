<template>
  <v-container class="pa-0">
    <v-row v-if="start">
      <v-col>
        <blog-group-option
        class="mx-5"
          title="seminars"
          bgImg="/bg2.jpg"
          textColor="white--text"
          @clicked="choseBlogSubject('seminar')"
          style="cursor: pointer"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import BlogGroupOption from "../components/BlogGroupOption.vue";
export default {
  name: "Blog",
  components: {
    BlogGroupOption
  },
  data() {
    return {
      start: true,
      subject: ""
    };
  },
  methods: {
    choseBlogSubject(prop) {
      this.start = !this.start;
      this.subject = prop;
    }
  }
};
</script>

<style scoped>
</style>