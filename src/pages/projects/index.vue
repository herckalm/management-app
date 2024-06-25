<template>
  <h1>Projects Page</h1>
  <RouterLink to="/">Home Page</RouterLink>
</template>

<script setup lang="ts">
import { supabase } from '@/lib/supabasClient'
import { ref } from 'vue'
;(async () => {
  const { data, error } = await supabase.from('projects').select()

  if (error) {
    console.log(error)
  }
  return data
})()
</script>

<style scoped></style>
