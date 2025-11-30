<script setup lang="ts">
import { track } from 'nano-custom'
</script>

<template>
  <div class="logos">
    <img src="./assets/vue-logo.svg" alt="Vue Logo" class="logo" width="80" height="80" />
    <img src="https://www.nanosights.dev/images/logo.svg" alt="NanoSights Logo" class="logo" width="80" height="80" />
  </div>
  <h1>Vue + NanoSights</h1>
  <p>This demo shows how NanoSights integrates with Vue.js.</p>
  <div class="buttons">
    <a
      @click="track('CTA')"
      class="button primary"
      href="https://www.nanosights.dev"
      target="_blank">Go to NanoSights</a>
    <a class="button secondary" href="https://www.nanosights.dev/docs">
      Documentation
    </a>
  </div>

  <nano-analytics
    projectKey="mcw2ugsj162ft"
  />
  <nano-insights
    projectKey="mcw2ugsj162ft"
  />
  <nano-custom
    projectKey="mcw2ugsj162ft"
  />
</template>