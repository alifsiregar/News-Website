<template>
  <div class="p-6">
    <h1 class="text-5xl">
      Healthcare News
    </h1>
    <DetailCard
      v-for="healthcareInfo in healthcareSections"
      :key="healthcareInfo.id"
      :cardinfo="healthcareInfo"
    />
  </div>
</template>

<script>
import { healthcareSections } from '@/assets/data.js'
export default {
  data () {
    return {
      healthcareSections
    }
  }
}
</script>

<style scoped>
</style>
