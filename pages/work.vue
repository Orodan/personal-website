<template>
  <ProfessionalExperiences />
</template>

<script>
import ProfessionalExperiences from "~/components/work/ProfessionalExperiences.vue";

export default {
  components: {
    ProfessionalExperiences,
  }
};

if (process.client) document.title = 'Jimmy Kasprzak | work'
</script>
