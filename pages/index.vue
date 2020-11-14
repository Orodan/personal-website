<template>
  <section class="index-page">
    <Intro class="white bg-green">
      Hi, I’m Jimmy. I’m an French software engineer living and working in Nantes, France.
      <br/>
      I'm also a trainer and I love sharing my passion for software development with people in many ways like writing blogs and speaking at meetups and conferences.
    </Intro>

    <section class="row-2-1">
      <LatestContent :articleSummary="latestArticleSummary"/>
      <PersonalInfo />
    </section>

    <section class="row-1-2">
      <ProfessionalExperiencesSummary />
      <SkillsSummary />
    </section>
  </section>
</template>

<script>
import LatestContent from "~/components/home/LatestContent.vue";
import PersonalInfo from "~/components/home/PersonalInfo.vue";
import ProfessionalExperiencesSummary from "~/components/home/ProfessionalExperiencesSummary.vue";
import SkillsSummary from "~/components/home/SkillsSummary.vue";
import Intro from "~/components/common/Intro.vue";

export default {
  components: {
    LatestContent,
    PersonalInfo,
    ProfessionalExperiencesSummary,
    SkillsSummary,
    Intro
  },
  async asyncData ({ $content }) {
    const articlesSummaries = await $content('articles')
      .only(['title', 'description', 'img', 'slug'])
      .sortBy('createdAt', 'asc')
      .fetch()

    return { latestArticleSummary: articlesSummaries[0] }
  },
  data () {
    return {
      title: 'Jimmy Kasprzak | home',
    }
  },
  head () {
    return {
      title: this.title,
    }
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

@media only screen and (max-width: 768px) {
  .row-2-1,
  .row-1-2 {
    display: block;
  }
}
</style>
