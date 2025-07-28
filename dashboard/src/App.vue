<script setup>
import Sidebar from "./components/Sidebar.vue";
import Card from "./components/Card.vue";
import TableCard from "./components/TableCard.vue";
import LineCard from "./components/LineCard.vue";
import PieCard from "./components/PieCard.vue";
import { Bars3Icon } from "@heroicons/vue/24/outline";
import { ref, watch } from "vue";

const isMenuShown = ref(false);
watch(isMenuShown, (newVal) => {
  console.log("Menu state changed:", newVal);
});
</script>

<template>
  <div class="main-container">
    <nav class="sidebar-container">
      <Sidebar />
    </nav>
    <div class="burger-menu" v-if="!isMenuShown">
      <div class="sidebar-container">
        <Sidebar />
      </div>
    </div>
    <main class="cards-container">
      <div class="welcome-header">
        <div class="burger-menu-icon" @click="isMenuShown = !isMenuShown">
          <Bars3Icon />
        </div>
        <h3>Welcome back, Ann.</h3>
      </div>

      <div class="cards">
        <div class="card-small-container">
          <div class="card-small">
            <Card
              title="Customers"
              line-colour="#FF8559"
              value="12"
              percentage="2.5"
              :is-increase="false"
            />
          </div>
          <div class="card-small">
            <Card
              title="Revenue"
              line-colour="#6395EE"
              value="$45"
              percentage="10"
              :is-increase="true"
            />
          </div>
          <div class="card-small">
            <Card
              title="Profit"
              line-colour="#FFC857"
              value="40%"
              percentage="5.5"
              :is-increase="true"
            />
          </div>
          <div class="card-med1"><PieCard title="Invoice Statistics" /></div>
          <div class="card-med2"><LineCard title="Sales Analytics" /></div>
          <div class="card-large"><TableCard title="Recent Invoices" /></div>
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
.welcome-header {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
  margin-top: 20px;
  gap: 10px;
}
.welcome-header h3 {
  font-weight: lighter;
  font-size: 1.5rem;
}
</style>
