<template>
  <div class="p-6">
    <h1 class="text-5xl">
      Sports News
    </h1>
    <DetailCard
      v-for="sportinfo in sportSections"
      :key="sportinfo.id"
      :cardinfo="sportinfo"
    />
  </div>
</template>

<script>
import { sportSections } from '@/assets/data.js'
export default {
  data () {
    return {
      sportSections
    }
  }
}
</script>

<style scoped>
</style>
