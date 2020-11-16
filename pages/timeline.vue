<template>
  <ProfessionalExperiences />
</template>

<script>
export default {
  data() {
    var name = "Mohammad Ishfaque Jahan Rafee";
    var pageName = "Timeline";
    return {
      title: name + " | " + pageName,
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>
