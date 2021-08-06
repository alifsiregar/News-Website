<template>
  <div class="p-6">
    <h1 class="text-5xl">
      Business News
    </h1>
    <DetailCard
      v-for="businessinfo in businessSections"
      :key="businessinfo.id"
      :cardinfo="businessinfo"
    />
  </div>
</template>

<script>
import { businessSections } from '@/assets/data.js'
export default {
  data () {
    return {
      businessSections
    }
  }
}
</script>

<style scoped>
</style>
