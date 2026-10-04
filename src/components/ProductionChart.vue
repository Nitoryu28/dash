<template>
  <div class="card production-card">

    <div class="card-header">
      <h2>Production by hour</h2>
      <p>Garments produced during the selected day</p>
    </div>

    <div class="chart">

      <div class="y-axis">
        <span></span>
        <span></span>
        <span></span>
      </div>

      <svg viewBox="0 0 600 170" preserveAspectRatio="none">

        <line
            x1="45"
            y1="140"
            x2="575"
            y2="140"
            class="axis"
        />

        <line
            x1="45"
            y1="25"
            x2="45"
            y2="140"
            class="axis"
        />

        <polyline
            points="75,112 155,82 235,95 315,50 395,62 475,25 555,42"
            class="chart-line"
        />

        <circle cx="75" cy="112" r="4" />
        <circle cx="155" cy="82" r="4" />
        <circle cx="235" cy="95" r="4" />
        <circle cx="315" cy="50" r="4" />
        <circle cx="395" cy="62" r="4" />
        <circle cx="475" cy="25" r="4" />
        <circle cx="555" cy="42" r="4" />

      </svg>

      <div class="chart-labels">
        <span>08</span>
        <span>10</span>
        <span>12</span>
        <span>14</span>
      </div>

    </div>

  </div>
</template>