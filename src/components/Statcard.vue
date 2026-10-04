<script setup>
defineProps({
  title: String,
  value: String,
  description: String
})
</script>

<template>
  <div class="stat-card">

    <span class="stat-title">
      {{ title }}
    </span>

    <strong class="stat-value">
      {{ value }}
    </strong>

    <span class="stat-description">
      {{ description }}
    </span>

  </div>
</template>