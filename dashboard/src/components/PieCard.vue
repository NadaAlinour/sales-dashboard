<script setup>
const props = defineProps(["title"]);
import { reactive } from "vue";
import { Doughnut } from "vue-chartjs";

import { Chart as ChartJS, Title, Tooltip, Legend, ArcElement } from "chart.js";

// Register necessary Chart.js components
ChartJS.register(Title, Tooltip, Legend, ArcElement);

const pieData = reactive({
  labels: ["Red", "Blue", "Yellow"],
  datasets: [
    {
      label: "Votes",
      data: [12, 19, 20],
      backgroundColor: ["#f87171", "#60a5fa", "#facc15"],
      hoverOffset: 4,
      offset: [0, 0, 10],
    },
  ],
});

const chartOptions = {
  responsive: true,
  plugins: {
    legend: {
      position: "right",
      labels: {
        paddingLeft: 30
      }
    },
    title: {
      display: true,
      text: "Pie Chart",
    },
  },
};
</script>

<template>
  <div class="card graph-card-container">
    <div class="card-header">{{ title }}</div>
    <div class="pie-container">
      <Doughnut :data="pieData" :options="chartOptions" />
    </div>
  </div>
</template>

<style scoped>
.graph-card-container {
  height: 250px;
}

.pie-container {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  width: 100%;
  overflow: hidden;
  height: 100%;

}
</style>
