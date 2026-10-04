<script setup>
const batches = [
  {
    id: 'LOT-024',
    stage: 'Sewing',
    progress: 64
  },
  {
    id: 'LOT-023',
    stage: 'Cutting',
    progress: 35
  },
  {
    id: 'LOT-022',
    stage: 'Finishing',
    progress: 88
  }
]
</script>

<template>
  <div class="card progress-card">

    <div class="card-header">
      <h2>Batch progress</h2>
      <p>Progress of current production batches</p>
    </div>

    <div class="batch-list">

      <div
          v-for="batch in batches"
          :key="batch.id"
          class="batch-row"
      >

        <strong>{{ batch.id }}</strong>

        <span>{{ batch.stage }}</span>

        <div class="progress-bar">
          <div
              class="progress-fill"
              :style="{ width: batch.progress + '%' }"
          ></div>
        </div>

        <small>{{ batch.progress }}%</small>

      </div>

    </div>

  </div>
</template>