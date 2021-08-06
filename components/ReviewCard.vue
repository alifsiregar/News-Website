<template>
  <div class="h-16 mt-16 md:mt-8 flex">
    <div class="image-container">
      <img :src="review.picture.large" alt="">
    </div>
    <div class="ml-8">
      <h6>{{ review.login.username }}</h6>
      <p class="text-gray-500">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus quam magni beatae possimus debitis.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    review: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
    img {
        width: 4rem;
        height: 4rem;
        border-radius: 100%;
    }
</style>
