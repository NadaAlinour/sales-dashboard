<script setup>
const props = defineProps(['title'])

</script>

<template>
  <div class="card table-card-container">
      {{title}}
  </div>
</template>

<style scoped>
.table-card-container {
  height: 250px;

}
</style>
