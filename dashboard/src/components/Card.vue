<script setup>
const props = defineProps([
  "title",
  "lineColour",
  "value",
  "percentage",
  "isIncrease",
]);
import { ArrowDownIcon, ArrowUpIcon } from "@heroicons/vue/24/outline";
</script>

<template>
  <div class="card card-container">
    <div>
      <div class="card-small-heading">
        <div class="line-decor" :style="{ backgroundColor: lineColour }"></div>
        <div>
          <div style="color: #878486">{{ title }}</div>
          <p>{{ value }}</p>
        </div>
      </div>
      <div class="card-small-percentange-container">
        <div class="arrow-icon-container" v-if="isIncrease">
          <ArrowUpIcon style="stroke: green" />
        </div>

        <div class="arrow-icon-container" v-if="!isIncrease">
          <ArrowDownIcon style="stroke: red" />
        </div>

        <p
          class="card-small-percentage"
          :style="{ color: props.isIncrease ? 'green' : 'red' }"
        >
          {{ percentage }}%
        </p>
        <p class="card-text" style="color: #878486">Since last week</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  height: 150px;
}

.card-small-heading {
  display: flex;
  width: 100%;
  gap: 15px;
}

.card-small-heading p {
  font-weight: lighter;
  font-size: 2rem;
}

.card-small-percentange-container {
  display: flex;
  margin: 10px;
  align-items: center;
}

.arrow-icon-container {
  height: 20px;
  width: 20px;
}

.card-text {
  margin-left: 10px;
  font-style: italic;
}
</style>
