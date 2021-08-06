<template>
  <div v-if="product" class="flex flex-col justify-center p-5">
    <img :src="require(`@/assets/images/${product.image}`)" alt="" class="max-w-lg">
    <button
      class="my-8 max-w-sm border-none p-2 text-white font-bold rounded-full p-4 bg-gray-800"
      @click="() => {
        toggleBookmark()
        addItem(product.id)
      }"
    >
      {{ added ? "Added!": "Bookmark" }}
    </button>
    <div class="mb-8">
      <h1 class="text-3xl">
        {{ product.title }}
      </h1>
      <p class="text-gray-500 text-justify">
        {{ product.description }}
      </p>
    </div>
    <Reviews />
  </div>
  <div v-else class="container padding">
    <h1 class="text-5xl">
      Page Not Found!
    </h1>
  </div>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  data () {
    return {
      added: false
    }
  },
  computed: {
    product () {
      return this.$store.getters.getSportNewsById(this.$route.params.id)
    }
  },
  methods: {
    ...mapMutations(['addItem']),
    toggleBookmark () {
      this.added = true
    }
  }
}
</script>

<style scoped>
</style>
