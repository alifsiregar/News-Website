<template>
  <NuxtLink
    :to="`/${cardinfo.category}/${cardinfo.id}`"
    class="my-6 flex flex-col justify-center items-center md:flex-row w-100 border-none overflow-hidden p-6 cursor-pointer shadow-lg rounded-lg"
  >
    <img class="image rounded-lg" :src="require(`@/assets/images/${cardinfo.image || 'fe1.jpg'}`)" alt="">
    <div class="flex flex-col justify-center md:ml-6">
      <h3 class="text-3xl">
        {{ cardinfo.title }}
      </h3>
      <p class="text-gray-500 text-justify text-lg">
        {{ cardinfo.snippet }}
      </p>
    </div>
  </NuxtLink>
</template>

<script>
export default {
  props: {
    cardinfo: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
    .image {
        height: 20rem;
        width: 20rem;
    }
</style>
