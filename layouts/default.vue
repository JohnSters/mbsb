<template>
  <v-app>
    <v-system-bar app color="white">
      <v-spacer></v-spacer>
      <p class="mt-4 hidden-sm-and-down">Please contact Morne Bothma @ <b class="red--text">082-867-4352 </b>for any
        inquiries.</p>
    </v-system-bar>

    <v-app-bar app color="blue darken-4" flat>
      <v-btn to="/" class="hidden-md-and-up" x-small text dark>Home</v-btn>
      <v-btn to="/about" class="hidden-md-and-up" x-small text dark>About</v-btn>
      <v-btn to="/products" class="hidden-md-and-up" x-small text dark>Products</v-btn>
      <v-btn to="/ingredients" class="hidden-md-and-up" x-small text dark>Ingredients</v-btn>
      <v-btn
        class="hidden-md-and-up"
        href="https://www.facebook.com/groups/1209494736252117/?mibextid=6NoCDW"
        target="_blank"
        x-small
        text
        dark>
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn
        class="hidden-sm-and-down"
        dark
        outlined
        rounded
        text
        to="/"
      >
        Home
      </v-btn>
      <v-btn
        class="ml-2 hidden-sm-and-down"
        dark
        outlined
        rounded
        text
        to="/about"
      >
        About
      </v-btn>
      <v-btn
        class="ml-2 orange hidden-sm-and-down"
        dark
        outlined
        rounded
        text
        to="/products"
      >
        Products
      </v-btn>
      <ProductIngredients />
      <v-btn
        class="ml-2 hidden-sm-and-down"
        dark
        href="https://www.facebook.com/groups/1209494736252117/?mibextid=6NoCDW"
        outlined
        rounded
        target="_blank"
        text
      >
        Facebook Page
      </v-btn>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt/>
      </v-container>
    </v-main>
    <v-footer padless>
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Morne Bothma Iodine/ Calcium Bird Blocks(Pty) LTD</strong>
      </v-col>
    </v-footer>

    <div>
      <SocialChat
        icon
        id="social-button"
        :attendants="attendants"
      >
        <p slot="header" >Chat to us on whatsapp for any question, or sales related topics.</p>
        <template v-slot:button>
          <img
            src="https://raw.githubusercontent.com/ktquez/vue-social-chat/master/src/icons/whatsapp.svg"
            alt="icon whatsapp"
            aria-hidden="true"
          >
        </template>
        <small slot="footer">Opening hours: 8am to 6pm</small>
      </SocialChat>
    </div>

  </v-app>
</template>

<script>

import { SocialChat } from 'vue-social-chat'

export default {
  name: 'DefaultLayout',
  components: {
    SocialChat
  },
  data () {
    return {
      attendants: [
        {
          app: 'whatsapp',
          text: 'Can you help me?',
          label: 'Marketing Manager',
          name: 'Morne Bothma',
          number: '27828674352',
          avatar: {
            src: '/products/logo-round.png',
            alt: 'Sales'
          }
        }
        // ...
      ]
    }
  }
}
</script>

<style>
:root #social-button {
  --vsc-bg-header: green;
  --vsc-bg-footer: #fafafa;
  --vsc-text-color-header: white;
  --vsc-text-color-footer: green;
  --vsc-bg-button: green;
  --vsc-text-color-button: purple;
  --vsc-outline-color: darkgreen;
  --vsc-border-color-bottom-header: teal;
  --vsc-border-color-top-footer: #f3f3f3;
}
</style>
