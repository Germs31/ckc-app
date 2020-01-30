<template>
  <div>
    <v-row>
      <v-col md="4">
        <h2 class="text-center mb-5">Recently Read Books</h2>
      </v-col>
      <v-col md="4">
        <h2 class="text-center mb-5">Favourite Books</h2>
      </v-col>
      <v-col md="4">
        <h2 class="text-center mb-5">Terrible Books</h2>
      </v-col>
    </v-row>
    <BookModal />
  </div>
</template>

<script>
import Card from '~/components/card.vue'
import Modal from '~/components/modal.vue'

export default {
  components: {
    Card,
    Modal
  }
}
</script>
