<script setup>
import '../assets/main.css'

import {
  PhotoIcon,
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
      <PhotoIcon style="stroke: #f5f2f2; width: 100px"/>
    </div>

    <div class="sidebar-group-container">
      <div class="sidebar-group">
        <h3>Main Menu</h3>
        <ul>
          <li>
            <div class="sidebar-icon">
              <Squares2X2Icon style="stroke: #f5f2f2; width: 20px" />
            </div>
            Dashboard
          </li>
          <li>
            <div class="sidebar-icon">
              <ShoppingBagIcon style="stroke: #f5f2f2; width: 20px" />
            </div>

            Products
          </li>
          <li>
            <div class="sidebar-icon">
              <BuildingStorefrontIcon style="stroke: #f5f2f2; width: 20px" />
            </div>

            Store
          </li>
          <li>
            <div class="sidebar-icon">
              <ChartBarSquareIcon style="stroke: #f5f2f2; width: 20px" />
            </div>

            Statistics
          </li>
          <li>
            <div class="sidebar-icon">
              <EnvelopeOpenIcon style="stroke: #f5f2f2; width: 20px" />
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
                <ExclamationCircleIcon style="stroke: #f5f2f2; width: 20px" />
              </div>
              Help Center
            </li>
            <li>
              <div class="sidebar-icon">
                <Cog8ToothIcon style="stroke: #f5f2f2; width: 20px" />
              </div>
              Settings
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="sidebar-logout-container">
      <div class="sidebar-icon">
        <ArrowLeftEndOnRectangleIcon style="stroke: #f5f2f2; width: 20px" />
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

.test {
  color: white;
}

.sidebar {
  font-size: 1.2em;
  display: flex;
  flex-direction: column;

}

.sidebar-group {
  margin-bottom: 40px;
}

.sidebar-group h3 {
  margin-bottom: 15px;
  font-size: 1.2rem;
  font-weight: lighter;
  color: #e1e4e6;
}

.sidebar-group ul {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-left: 10px;
}

.sidebar-group li,
.sidebar-logout-container {
  display: flex;
  gap: 10px;
  align-items: center;
  color: #e1e4e6;

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
