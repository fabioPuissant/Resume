<template>
  <v-card max-width="375" class="mx-auto mt-8">
    <v-img src="/thai.jpg" height="300px" dark>
      <v-row class="fill-height">
        <v-card-title>
          <v-btn dark text disabled icon></v-btn>

          <v-spacer></v-spacer>

          <v-btn dark text disabled icon class="mr-4"></v-btn>

          <v-btn text disabled dark icon></v-btn>
        </v-card-title>

        <v-spacer></v-spacer>

        <v-card-title class="white--text pl-12 mt-12 pt-12">
          <div class="display-1 white--text text-capitalize pl-12 pt-12">
            <span>fabio</span>
            <span>&nbsp;</span>
            <span>puissant</span>
          </div>
        </v-card-title>
      </v-row>
    </v-img>

    <v-list text two-line>
      <v-list-item-group>
        <MailListItemComponent
          v-for="contact in mailAddresses"
          :key="contact.address"
          :mailAddress="contact.address"
          :contactAddressOption="contact.contact"
          :showMailIcon="contact.mailIcon"
        />
        <v-list-item>
          <v-list-item-icon>
            <v-icon color="indigo">phone</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>(+32) 0491-1257-18</v-list-item-title>
            <v-list-item-subtitle>Mobile</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-divider inset></v-divider>

        <v-divider inset></v-divider>

        <v-list-item>
          <v-list-item-icon>
            <v-icon color="indigo">location_on</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Hogeschool PXL</v-list-item-title>
            <v-list-item-subtitle>Hasselt, Limburg 3500</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-row justify-sm="center">
            <v-list-item-icon>
              <v-spacer></v-spacer>
              <v-btn fab small class="mx-3">
                <v-avatar @click="routeTo('https://github.com/fabioPuissant')" class="mx-3">
                  <v-img src="/gh.png" />
                </v-avatar>
              </v-btn>
              <v-btn fab small class="mx-3">
                <v-avatar @click="routeTo('https://www.facebook.com/fabio.puissant')" class="mx-3">
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
          </v-row>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
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
          contact: true,
          mailIcon: true
        },
        {
          address: "fabio.puissant@hotmail.com",
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
  }
};
</script>

<style scoped>
</style>