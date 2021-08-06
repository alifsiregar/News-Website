<template>
  <div class="p-6">
    <h1 class="text-5xl">
      My Bookmarks
    </h1>
    <DetailCard
      v-for="bookmark in myBookmarks"
      :key="bookmark.id"
      :cardinfo="bookmark"
    />
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState([
      'myBookmarks'
    ])
  }
}
</script>

<style scoped>
</style>
