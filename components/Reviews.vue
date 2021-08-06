<template>
  <div>
    <h3 class="text-3xl">
      Comments
    </h3>
    <div v-if="reviewers.results">
      <ReviewCard
        v-for="reviewer in reviewers.results"
        :key="reviewer.login.uuid"
        :review="reviewer"
      />
    </div>
  </div>
</template>

<script>
import { commentsURL } from '@/services'
export default {

  data () {
    return {
      reviewers: []
    }
  },
  async fetch () {
    this.reviewers = await fetch(commentsURL).then(res => res.json())
  }
}
</script>

<style lang="scss" scoped>

</style>
