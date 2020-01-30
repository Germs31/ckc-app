<template>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>{{bookTitle}}</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0">{{bookAuthor}}</v-card-subtitle>

    <v-card-text class="text--primary">
      {{bookDescription}}
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="orange"
        text
      >
        Share
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ["bookTitle", "bookAuthor", "bookDescription"]
}
</script>

