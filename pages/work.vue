<template>
  <ProfessionalExperiences />
</template>

<script>
import ProfessionalExperiences from "~/components/ProfessionalExperiences.vue";

export default {
  components: {
    ProfessionalExperiences,
  }
};

if (process.client) document.title = 'Jimmy Kasprzak | work'
</script>
