<script setup>
import Sidebar from "./components/Sidebar.vue";
import Card from "./components/Card.vue";
import TableCard from "./components/TableCard.vue";
import GraphCard from "./components/GraphCard.vue";

</script>

<template>
  <main class="main-container">
    <nav class="sidebar-container">
      <Sidebar />
    </nav>
    <section class="cards-container">
      <div class="welcome-header">
        <h3>Welcome back, [User]!</h3>
      </div>

      <div class="cards">
        <div class="card-small-container">
          <div class="card-small"><Card /></div>
          <div class="card-small"><Card /></div>
          <div class="card-small"><Card /></div>
        </div>

        <div class="card-med-container">
          <div class="card-med"><GraphCard /></div>
          <div class="card-med"><GraphCard /></div>
        </div>

        <div class="card-large"><TableCard /></div>
      </div>
    </section>
  </main>
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
