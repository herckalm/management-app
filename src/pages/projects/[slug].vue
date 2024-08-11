<script setup lang="ts">
import { useRoute } from 'vue-router'
</script>

<template>
  <div>
    <h1>Project {{ useRoute().params?.slug }}</h1>
  </div>
</template>
