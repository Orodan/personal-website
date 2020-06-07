<template>
  <section class="index-page">
    <Header />
    <section class="row-2-1">
      <AboutMe />
      <section class="personal-info">
        Personal Info incoming
      </section>
    </section>
  </section>
</template>

<script>
import Header from "~/components/Header.vue";
import AboutMe from "~/components/AboutMe.vue";

export default {
  components: {
    Header,
    AboutMe
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
