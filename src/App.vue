<script setup>
import Sidebar from './components/Sidebar.vue'
import StatCard from './components/StatCard.vue'
import ProductionChart from './components/ProductionChart.vue'
import BatchesStage from './components/BatchesStage.vue'
import BatchProgress from './components/BatchProgress.vue'
</script>

<template>
  <div class="app">
    <Sidebar />

    <main class="main-content">
      <header class="header">
        <div>
          <h1>Dashboard</h1>
          <p>Overview of today's production</p>
        </div>
      </header>

      <section class="filters">
        <div class="filter">
          <label>Date</label>
          <select>
            <option>Today</option>
            <option>Yesterday</option>
            <option>This week</option>
          </select>
        </div>

        <div class="filter">
          <label>Batch</label>
          <select>
            <option>All batches</option>
            <option>LOT-024</option>
            <option>LOT-023</option>
            <option>LOT-022</option>
          </select>
        </div>
      </section>

      <section class="stats">
        <StatCard
            title="Total produced today"
            value="1,240"
            description="garments"
        />

        <StatCard
            title="Average per hour"
            value="155"
            description="garments / hour"
        />

        <StatCard
            title="Daily compliance"
            value="82%"
            description="daily production target"
        />
      </section>

      <section class="dashboard-grid">
        <ProductionChart />
        <BatchesStage />
      </section>

      <BatchProgress />
    </main>
  </div>
</template>