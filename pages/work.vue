<template>
  <ProfessionalExperiences />
</template>

<script>
import ProfessionalExperiences from "~/components/work/ProfessionalExperiences.vue";

export default {
  components: {
    ProfessionalExperiences,
  },
  data() {
    return {
      title: "Jimmy Kasprzak | work",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>
