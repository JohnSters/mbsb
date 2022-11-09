<template>
  <v-app>
    <v-system-bar app color="white">
      <v-spacer></v-spacer>
      <p class="mt-4 hidden-sm-and-down">Please contact Morne Bothma @ <b class="red--text">082-867-4352 </b>for any
        inquiries.</p>
    </v-system-bar>

    <v-app-bar app color="blue darken-4" flat>
      <v-spacer></v-spacer>
      <v-btn to="/" class="hidden-md-and-up" x-small text dark>Home</v-btn>
      <v-btn to="/about" class="hidden-md-and-up" x-small text dark>About</v-btn>
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
    <v-footer
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      links: [
        'Dashboard',
        'Messages',
        'Profile',
        'Updates'
      ]
    }
  }
}
</script>
