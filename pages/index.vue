<template>
  <section class="index-page">
    <Header />
    <section class="row-2-1">
      <AboutMe />
      <PersonalInfo />
    </section>

    <section class="row-1-2">
      <ProfessionalExperiences />
      <Skills />
    </section>
  </section>
</template>

<script>
import Header from "~/components/Header.vue";
import AboutMe from "~/components/AboutMe.vue";
import PersonalInfo from "~/components/PersonalInfo.vue";
import ProfessionalExperiences from "~/components/ProfessionalExperiences.vue";
import Skills from "~/components/Skills.vue";

export default {
  components: {
    Header,
    AboutMe,
    PersonalInfo,
    ProfessionalExperiences,
    Skills
  }
};
</script>

<style scoped>
.index-page {
  flex: 1;
}

.row-1-2 {
  display: flex;
}

.row-1-2 > *:first-child {
  flex: 1;
}

.row-1-2 > *:nth-child(2) {
  flex: 2;
}

.row-2-1 {
  display: flex;
}

.row-2-1 > *:first-child {
  flex: 2;
}

.row-2-1 > *:nth-child(2) {
  flex: 1;
}
</style>
