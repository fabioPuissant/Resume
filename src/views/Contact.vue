<template>
<v-container>
  <v-card :max-width="isSmallerScreen ? '300' : '375'" class="bg-color mx-auto mt-8">
    <v-img src="/thai.jpg" height="300px" dark>
      <v-row class="fill-height">
        <v-card-title class="">
          <v-btn dark text disabled icon></v-btn>

          <v-spacer></v-spacer>

          <v-btn dark text disabled icon class="mr-4"></v-btn>

          <v-btn text disabled dark icon></v-btn>
        </v-card-title>

        <v-spacer></v-spacer>

        <v-card-title class="white--text pl-12 mt-12 pt-12 text-center">
          <div
            :class="['white--text text-capitalize pl-10 pt-12', isSmallerScreen ? 'headline' : 'display-1']"
          >
            <span>fabio</span>
            <span>&nbsp;</span>
            <span>puissant</span>
          </div>
        </v-card-title>
      </v-row>
    </v-img>

    <v-list text two-line class="bg-color">
      <v-list-item-group>
        <MailListItemComponent
          v-for="contact in mailAddresses"
          :key="contact.address"
          :mailAddress="contact.address"
          :type="contact.type"
          :contactAddressOption="contact.contact"
          :showMailIcon="contact.mailIcon"
          :smallScreen="isSmallerScreen"
        />
        <v-divider class="mx-auto" inset></v-divider>
        <v-list-item>
          <v-list-item-icon>
            <v-icon color="indigo">location_on</v-icon>
          </v-list-item-icon>

          <v-list-item-content class="bg-color white--text">
            <v-list-item-title class="white--text">Hogeschool PXL</v-list-item-title>
            <v-list-item-subtitle class="white--text">Hasselt, Limburg 3500</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-list-item class="bg-color">
          <v-row justify-sm="center">
            <v-col align="center">
              <v-list-item-icon>
                <v-spacer></v-spacer>
                <v-btn fab small class="mx-3">
                  <v-avatar @click="routeTo('https://github.com/fabioPuissant')" class="mx-3">
                    <v-img src="/gh.png" />
                  </v-avatar>
                </v-btn>
                <v-btn fab small class="mx-3">
                  <v-avatar
                    @click="routeTo('https://www.facebook.com/fabio.puissant')"
                    class="mx-3"
                  >
                    <v-img src="/fv.png" />
                  </v-avatar>
                </v-btn>
                <v-btn fab small class="mx-3">
                  <v-avatar
                    @click="routeTo('https://www.linkedin.com/in/fabio-puissant-158b0716b/')"
                    class="mx-3"
                  >
                    <v-img src="/li.png" />
                  </v-avatar>
                </v-btn>
              </v-list-item-icon>
            </v-col>
          </v-row>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</v-container>

</template>

<script>
import MailListItemComponent from "../components/MailListItem.vue";
export default {
  components: { MailListItemComponent },
  data() {
    return {
      mailAddresses: [
        {
          address: "fabio.puissant@student.pxl.be",
          type: "Student mail",
          contact: true,
          mailIcon: true
        },
        {
          address: "fabio.puissant@hotmail.com",
          type: "Personal mail",
          contact: true,
          mailIcon: false
        }
      ]
    };
  },
  methods: {
    routeTo(url) {
      window.location = url;
    }
  },
  computed: {
    isSmallerScreen() {
      return window.innerWidth <= 400;
    }
  }
};
</script>

<style scoped>
.bg-color {
  background: #2d253c !important;
}
</style>