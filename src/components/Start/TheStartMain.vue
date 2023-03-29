<script setup>
import TheAboutOurProjectSection from './MainSections/TheAboutOurProjectSection.vue'
import TheCompanyValuesSection from './MainSections/TheCompanyValuesSection.vue'
import TheOurJobsSection from './MainSections/TheOurJobsSection.vue'
import TheProjectVideoSection from './MainSections/TheProjectVideoSection.vue'
import TheTeamsSection from './MainSections/TheTeamsSection.vue'
import TheWorkplaceAndCultureSection from './MainSections/TheWorkplaceAndCultureSection.vue'
</script>

<template>
  <main class="flex flex-col flex-grow">
    <TheProjectVideoSection />
    <TheAboutOurProjectSection />
    <TheWorkplaceAndCultureSection />
    <TheCompanyValuesSection />
    <TheTeamsSection />
    <TheOurJobsSection />
  </main>
</template>

<style scoped></style>
