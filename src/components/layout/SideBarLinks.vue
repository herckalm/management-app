<script setup lang="ts">
interface LinkProp {
  title: string
  to: string
  icon: string
}

defineProps<{
  links: LinkProp[]
  accountLinks: LinkProp[]
}>()
</script>

<template>
  <RouterLink
    exactActiveClass="text-primary bg-muted"
    v-for="link in links"
    :key="link.title"
    :to="link.to"
    class="flex items-center gap-3 px-4 py-2 mx-2 transition-colors rounded-lg hover:text-primary justify-center lg:justify-normal text-muted-foreground"
  >
    <iconify-icon :icon="link.icon"></iconify-icon>
    <span class="hidden lg:block text-nowrap">{{ link.title }}</span>
  </RouterLink>

  <RouterLink
    exactActiveClass="text-primary bg-muted"
    v-for="accountLink in accountLinks"
    :key="accountLink.title"
    :to="accountLink.to"
    class="flex items-center gap-3 px-4 py-2 mx-2 transition-colors rounded-lg hover:text-primary justify-center lg:justify-normal text-muted-foreground"
  >
    <iconify-icon :icon="accountLink.icon"></iconify-icon>
    <span class="hidden lg:block text-nowrap">Profile</span>
  </RouterLink>
</template>
