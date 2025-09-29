<script setup lang="ts">
const columns = [{
  label: 'Links',
  children: [{
    label: 'LinkedIn',
    to: 'https://www.linkedin.com/company/adler-pelzer-group/'
  }, {
    label: 'YouTube',
    to: 'https://www.youtube.com/@AdlerPelzerGroup'
  }]
}, {
  label: 'Company',
  children: [{
    label: 'About Us',
    to: 'https://www.adlerpelzer.com/about-us/'
  }, {
    label: 'Products & Technologies',
    to: 'https://www.adlerpelzer.com/products-technologies/'
  }, {
    label: 'Mission & Vision',
    to: 'https://www.adlerpelzer.com/mission-vision'
  }, {
    label: 'Careers',
    to: 'https://www.adlerpelzer.com/careers/'
  }]
}, {
  label: 'Acoustic Symposium',
  children: [{
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
  }, {
    label: 'Register',
    to: '/register',
    disabled: true
  }]
}]
</script>

<template>
  <USeparator class="h-px" />

  <UFooter :ui="{ top: 'border-b border-default' }">
    <template #top>
      <UContainer>
        <UFooterColumns :columns="columns">
          <template #left>
            <div class="text-sm text-muted">
              <div class="mb-4 font-semibold">
                Adler Pelzer Holding GmbH
              </div>
              Kabeler Str. 4<br>
              58099 Hagen<br>
              Germany<br>
              <br>
              Phone: +49 2331 6978 0<br>
              Email: info(at)adlerpelzer.com
            </div>
          </template>
        </UFooterColumns>
      </UContainer>
    </template>

    <template #left>
      <p class="text-muted text-sm">
        Adler Pelzer Group • © {{ new Date().getFullYear() }}
      </p>
    </template>

    <template #right>
      <UColorModeButton />
    </template>
  </UFooter>
</template>
