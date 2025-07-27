<script setup>
import {
  PhotoIcon,
  HomeIcon,
  Cog6ToothIcon,
  ChartBarIcon,
  EnvelopeIcon,
  ArrowLeftEndOnRectangleIcon,
  Squares2X2Icon,
  ShoppingBagIcon,
  BuildingStorefrontIcon,
  ChartBarSquareIcon,
  EnvelopeOpenIcon,
  Cog8ToothIcon,
  ExclamationCircleIcon,
} from "@heroicons/vue/24/outline";

defineProps({});
</script>

<template>
  <div class="sidebar">
    <div class="sidebar-logo">
      <PhotoIcon style="width: 75%; color: gray" />
    </div>

    <div class="sidebar-group-container">
      <div class="sidebar-group">
        <h3>Main Menu</h3>
        <ul>
          <li>
            <div class="sidebar-icon">
              <Squares2X2Icon style="width: 20px; color: gray" />
            </div>
            Dashboard
          </li>
          <li>
            <div class="sidebar-icon">
              <ShoppingBagIcon style="width: 20px; color: gray" />
            </div>

            Products
          </li>
          <li>
            <div class="sidebar-icon">
              <BuildingStorefrontIcon style="width: 20px; color: gray" />
            </div>

            Store
          </li>
          <li>
            <div class="sidebar-icon">
              <ChartBarSquareIcon style="width: 20px; color: gray" />
            </div>

            Statistics
          </li>
          <li>
            <div class="sidebar-icon">
              <EnvelopeOpenIcon style="width: 20px; color: gray" />
            </div>

            Invoices
          </li>
        </ul>
      </div>

      <div class="sidebar-group">
        <div class="sidebar-group-content">
          <h3>Help & Support</h3>
          <ul>
            <li>
              <div class="sidebar-icon">
                <ExclamationCircleIcon style="width: 20px; color: gray" />
              </div>
              Help Center
            </li>
            <li>
              <div class="sidebar-icon">
                <Cog8ToothIcon style="width: 20px; color: gray" />
              </div>
              Settings
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="sidebar-logout-container">
      <div class="sidebar-icon">
        <ArrowLeftEndOnRectangleIcon style="width: 20px; color: gray" />
      </div>
      Log Out
    </div>
  </div>
</template>

<style scoped>
.sidebar-logo {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
}

.sidebar {
  font-size: 1.5rem;
  display: flex;
  flex-direction: column;
  color: white;
}

.sidebar-group {
  margin-bottom: 40px;
}

.sidebar-group h3 {
  margin-bottom: 15px;
  font-size: 1.2rem;
  font-weight: lighter;
}

.sidebar-group ul {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-left: 10px;
}

.sidebar-group li,
.sidebar-logout-container {
  display: flex;
  gap: 10px;
  align-items: center;
}

.sidebar-group li:hover {
  cursor: pointer;
}

.sidebar-logout-container {
  height: 50px;
  margin-left: 10px;
  display: flex;
  align-items: center;
  justify-content: left;
}

.sidebar-logout-container:hover {
  cursor: pointer;
}

.sidebar-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}

.sidebar-group-container {
  flex: 1;
}
</style>
