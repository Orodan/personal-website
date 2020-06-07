<template>
  <section>
    <Header />
    <section class="row-2-1">
      <AboutMe class="about-me" />
      <div class="personal-info">
        Personal Info incoming
      </div>
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
section {
  flex: 1;
}

.row-2-1 {
  display: flex;
}

.about-me {
  flex: 2;
}

.personal-info {
  flex: 1;
}
</style>
