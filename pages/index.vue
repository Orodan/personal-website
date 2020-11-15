<template>
  <section class="index-page">
    <Summary :class="'white bg-green'" />

    <section class="row-2-1">
      <LatestContent :articleSummary="latestArticleSummary" />
      <PersonalInfo />
    </section>

    <section class="row-1-2">
      <ProfessionalExperiencesSummary />
      <SkillsSummary />
    </section>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articlesSummaries = await $content("articles")
      .only(["title", "description", "img", "slug"])
      .sortBy("createdAt", "asc")
      .fetch();

    return { latestArticleSummary: articlesSummaries[0] };
  },
  data() {
    return {
      title: "Mohammad Ishfaque Jahan Rafee | home",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
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

@media only screen and (max-width: 768px) {
  .row-2-1,
  .row-1-2 {
    display: block;
  }
}
</style>
