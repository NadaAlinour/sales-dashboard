<script setup>
const props = defineProps(['title'])
</script>

<template>
  <div class="card card-container">
    {{ title }}
  </div>
</template>

<style scoped>
  .card-container {
    height: 150px;
  }
</style>
