<template>
  <NuxtLink :to="`/${card.category}/${card.id}`" class="w-100 my-3 md:my-0 md:w-3/12 h-96 border-none overflow-hidden p-0 cursor-pointer">
    <img class="image" :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="">
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
    .image {
        height: 65%;
        border-radius: 0.5rem;
    }
    .header {
        font-size: 1.15rem;
        margin-top: 0.4rem;
    }
    .snippet {
        color: grey
    }
</style>
