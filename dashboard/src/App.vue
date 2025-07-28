<script setup>
import Sidebar from "./components/Sidebar.vue";
import Card from "./components/Card.vue";
import TableCard from "./components/TableCard.vue";
import LineCard from "./components/LineCard.vue";
import PieCard from "./components/PieCard.vue";

</script>

<template>
  <div class="main-container">
    <nav class="sidebar-container">
      <Sidebar />
    </nav>
    <main class="cards-container">
      <div class="welcome-header">
        <h3>Welcome back, Ann.</h3>
      </div>

      <div class="cards">
        <div class="card-small-container">
          <div class="card-small"><Card title="Customers" /></div>
          <div class="card-small"><Card title="Revenue" /></div>
          <div class="card-small"><Card title="Profit" /></div>
        </div>

        <div class="card-med-container">
          <div class="card-med1"><PieCard title="Invoice Statistics" /></div>
          <div class="card-med2"><LineCard title="Sales Analytics" /></div>
        </div>

        <div class="card-large"><TableCard title="Recent Invoices" /></div>
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
}
.welcome-header h3 {
  font-weight: lighter;
  font-size: 1.5rem;
}

.burger-menu-icon {
  display: none;
}

@media (max-width: 775px) {
  .burger-menu-icon {
    display: block;
  }

  .sidebar-container {
    display: none;
  }
}

.burger-menu-icon:hover {
  cursor: pointer;
}
</style>
