<template>
  <section class="index-page">
    <Header />

    <section class="self-intro">
      Hi, I’m Jimmy. I’m an French software engineer living and working in Nantes, France.
      <br/>
      I'm also a trainer and I love sharing my passion for software development with people in many ways like writing blogs and speaking at meetups and conferences.
    </section>

    <section class="row-2-1">
      <AboutMe />
      <PersonalInfo />
    </section>

    <section class="row-1-2">
      <ProfessionalExperiences />
      <Skills />
    </section>

    <Footer />
  </section>
</template>

<script>
import Header from "~/components/Header.vue";
import AboutMe from "~/components/AboutMe.vue";
import PersonalInfo from "~/components/PersonalInfo.vue";
import ProfessionalExperiences from "~/components/ProfessionalExperiences.vue";
import Skills from "~/components/Skills.vue";
import Footer from "~/components/Footer.vue";

export default {
  components: {
    Header,
    AboutMe,
    PersonalInfo,
    ProfessionalExperiences,
    Skills,
    Footer
  }
};
</script>

<style scoped>
.self-intro {
  padding: 60px 40px;
  color: #fff;
  font-size: 26px;
  background-color: var(--green);
}

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
