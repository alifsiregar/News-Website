<template>
  <div class="my-6">
    <h4 class="font-bold ">
      {{ cardsSection.title }}
    </h4>
    <p class="mb-6 text-gray-500">
      {{ cardsSection.snippet }}
    </p>
    <div class="flex md:justify-around items-center flex-col md:flex-row justify-center">
      <LargeCard
        v-for="card in cardsSection.cards"
        :key="card.image"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cardsSection: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
    .header {
        font-size: 1.5rem;
    }
</style>
