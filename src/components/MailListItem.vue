<template>
      <v-list-item>
        <v-list-item-icon>
          <v-icon v-if="showMailIcon" color="indigo">mail</v-icon>
        </v-list-item-icon>

        <v-list-item-content class="white--text">
          <v-list-item-title :class="smallScreen ? 'caption font-weight-bold' : ''">{{mailAddress}}</v-list-item-title>
          <v-list-item-subtitle class="white--text">{{type}}</v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-icon v-if="contactAddressOption" @click="mailTo()">
          <v-icon>chat</v-icon>
        </v-list-item-icon>
      </v-list-item>
</template>

<script>
export default {
    name: 'MailListItemComponent',
    methods: {
        mailTo(){
            window.location.href = `mailto:${this.mailAddress}?subject=Subject&body=message%20goes%20here`;
        },
    },
        props: {
            mailAddress: {
                required: true,
            },
            contactAddressOption: {
                required: false,
            },
            showMailIcon: {
                required: false,
            },
             type: {
                required: true,
            },
            smallScreen: {
              required: true,
              type: Boolean,
            }
        }
}
</script>

<style scoped>

</style>