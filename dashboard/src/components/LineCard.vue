<script setup>
const props = defineProps(["title"]);
import { reactive } from "vue";

import { Line } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  CategoryScale,
  LinearScale,
  PointElement,
} from "chart.js";

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  LineElement,
  CategoryScale,
  LinearScale,
  PointElement
);

const lineData = reactive({
  labels: [
    "Jan",
    "Feb",
    "Mar",
    "Apr",
    "May",
    "Jun",
    "Jul",
    "Aug",
    "Sep",
    "Oct",
    "Nov",
    "Dec",
  ],
  datasets: [
    {
      label: "Revenue",
      data: [
        "2000",
        "3500",
        "5000",
        "4200",
        "3540",
        "4120",
        "4850",
        "2780",
        "3800",
        "4500",
        "5125",
        "3565",
      ],
      borderColor: "#3b82f6",
      backgroundColor: "rgba(59, 130, 246, 0.2)",
      tension: 0.3,
      fill: true,
    },
  ],
});

const chartOptions = {
  responsive: true,
  plugins: {
    legend: { display: false },
    title: { display: true, text: "Monthly Revenue" },
  },
  scales: {
    y: {
      beginAtZero: true,
      title: { display: true, text: "Revenue ($)" },
    },
    x: {
      title: { display: true, text: "Month" },
    },
  },
};
</script>

<template>
  <div class="card graph-card-container">
    <div class="card-header">{{ title }}</div>
    <div class="line-container">
      <Line style="width:80%" :data="lineData" :options="chartOptions" />
    </div>
  </div>
</template>

<style scoped>

.line-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  overflow: hidden;
  height: 100%;
}



</style>
