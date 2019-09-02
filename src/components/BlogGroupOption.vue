<template>
  <v-card :color="bgColor">
    <v-img @click="clicked()" height="100" :src="bgImg">
      <v-container>
        <v-row wrap no-gutters justify="center" align="center">
          <v-col cols="auto">
            <v-card-title :class="['text-capitalize white--text display-2', textColor ]">{{title}}</v-card-title>
          </v-col>
        </v-row>
      </v-container>
    </v-img>
  </v-card>
</template>

<script>
export default {
  name: "BlogGroupOption",
  props: {
    title: {
      required: true,
      type: String
    },
    bgImg: {
      required: false,
      type: String
    },
    bgColor: {
      required: false,
      type: String
    },
    textColor: {
      required: false,
      type: String
    }
  },
  computed: {
    bgImgSource() {
      return this.bgImg ? this.bgImg : "";
    }
  },
  methods:{
      clicked() {
          this.$emit('clicked');
      }
  }
};
</script>

<style scoped>
</style>