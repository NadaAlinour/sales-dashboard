<script setup>
const props = defineProps(["title"]);
</script>

<template>
  <div class="card table-card-container">
    <div class="card-header">{{ title }}</div>
  </div>
</template>

<style scoped>
.table-card-container {
  height: 300px;
}
</style>
