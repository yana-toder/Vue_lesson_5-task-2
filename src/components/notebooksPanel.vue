<template>
  <div>
    <product-card
      v-for="card in notebooksCardsData"
      :card-data="card"
      :key="card.id"
    />
  </div>
</template>

<script>
import productCard from './productCard.vue'

export default {
  components: {productCard},
  name: 'NotebooksPanel',

  props: {
    notebooksCardsData: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style lang="scss" scoped></style>
