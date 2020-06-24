<template>
  <section class="index-page">
    <Header />
    <section class="row-2-1">
      <AboutMe />
      <PersonalInfo />
    </section>
  </section>
</template>

<script>
import Header from "~/components/Header.vue";
import AboutMe from "~/components/AboutMe.vue";
import PersonalInfo from "~/components/PersonalInfo.vue";

export default {
  components: {
    Header,
    AboutMe,
    PersonalInfo
  }
};
</script>

<style scoped>
.index-page {
  flex: 1;
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
