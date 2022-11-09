<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          class="ml-2 hidden-sm-and-down"
          dark
          outlined
          rounded
          text
          v-bind="attrs"
          v-on="on"
        >
          Ingredients
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5 white--text blue lighten-2">
          Product Ingredients
        </v-card-title>

        <v-card-text class="mt-3">
          <p><b>Please note Blocks are Patent protected therefore no volumes or percentages are shared  (some key ingredients are left out with reason.)</b></p>
          <ul>
            <li>Diatom Concentrate </li>
            <li>Medical grade Binder </li>
            <li>Calcium Concentrate </li>
            <li>+/- 16 Multi Minerals and trace elements </li>
            <li>+/- 13 Multi Vitamins</li>
          </ul>
          <p class="mt-3">Vanilla extract, antioxidant effects, anti inflammatory properties.</p>
          <p>Glucose powder: Dehydration, Vitamin D, Mono hydrate for muscle recovery.</p>
          <p>Natural Iodine, 40% Sodium by Weight.</p>
          <p>Antioxidant minerals such as Manganese and Zinc, Iodine.</p>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            outlined
            rounded
            text
            @click="dialog = false"
          >
            Close
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: 'ProductIngredients',
  data: () => ({
    dialog: false
  })
}
</script>

<style scoped>

</style>
