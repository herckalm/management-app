<script setup lang="ts">
import { RouterView } from 'vue-router'
import { supabase } from '@/lib/supabaseClient'
</script>

<template>
  <main>
    <RouterView></RouterView>
  </main>
</template>

<style scoped></style>
