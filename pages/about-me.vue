<template>
  <section>
    <Header />

    <section class="self-intro">
      Hi, I’m Jimmy. I’m an French software engineer living and working in Nantes, France.
      <br/>
      I'm also a trainer and I love sharing my passion for software development with people in many ways like writing blogs and speaking at meetups and conferences.
    </section>
  </section>
</template>

<style scoped>
.self-intro {
  padding: 60px 40px;
  color: #fff;
  font-size: 26px;
  background-color: var(--blue);
}
</style>

<script>
import Header from "~/components/Header.vue";

export default {
  components: {
    Header,
  }
};
</script>
