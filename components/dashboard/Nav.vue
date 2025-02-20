<script setup>
const route = useRoute()
</script>

<template>
  <section class="flex justify-between">
    <Tabs
      v-if="route.path !== '/dashboard/link'"
      :default-value="route.path"
      @update:model-value="navigateTo"
    >
    </Tabs>
    <slot name="left" />
    <div>
      <slot />
    </div>
  </section>
</template>
