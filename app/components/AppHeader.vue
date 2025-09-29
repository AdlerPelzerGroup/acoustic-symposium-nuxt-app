<script setup lang="ts">
const items = computed(() => [{
  label: 'Home',
  to: '/'
}, {
  label: 'About',
  to: '/about'
}, {
  label: 'Conference Chair',
  to: '/conference-chair'
}, {
  label: 'Scientific Committee',
  to: '/scientific-committee'
}, {
  label: 'Student Posters',
  to: '/student-posters'
}])
</script>

<template>
  <UHeader>
    <template #left>
      <NuxtLink to="/">
        <AppLogo class="w-auto h-12 shrink-0" />
      </NuxtLink>
    </template>

    <UNavigationMenu
      :items="items"
      variant="link"
    />

    <template #right>
      <UButton
        label="Register now"
        color="primary"
        disabled
        trailing-icon="i-lucide-arrow-right"
        class="hidden lg:inline-flex"
        to="/register"
      />
    </template>

    <template #body>
      <UNavigationMenu
        :items="items"
        orientation="vertical"
        class="-mx-2.5"
      />

      <USeparator class="my-6" />

      <UButton
        label="Register now"
        color="neutral"
        to="/signup"
        block
        disabled
      />
    </template>
  </UHeader>
</template>
