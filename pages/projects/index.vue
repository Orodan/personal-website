<template>
  <section>
    <section class="articles">
      <div
        v-for="articleSummary of articlesSummaries"
        :key="articleSummary.slug"
        class="card-article"
        @click="goTo(articleSummary.slug)"
      >
        <h3>{{ articleSummary.title }}</h3>
        <img :src="articleSummary.img" :alt="articleSummary.title" />
        <p>{{ articleSummary.description }}</p>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articlesSummaries = await $content("data")
      .only(["title", "description", "img", "slug"])
      .sortBy("createdAt", "asc")
      .fetch();

    return { articlesSummaries };
  },
  methods: {
    goTo: function(slug) {
      this.$router.push({ name: "projects-slug", params: { slug } });
    },
  },
  data() {
    var name = "Mohammad Ishfaque Jahan Rafee";
    var pageName = "Projects";
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

<style scoped>
.articles {
  display: flex;
  padding: 60px 40px;
  background-color: var(--white);
  flex-wrap: wrap;
}

.card-article {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.3);
  border-radius: 5px;
  margin: 20px;
  width: 320px;
  cursor: pointer;
  transition: box-shadow 0.3s;
}

.card-article:hover {
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.8);
}

.card-article h3 {
  margin-bottom: 20px;
}

.card-article img {
  width: 100%;
  margin-bottom: 20px;
}

@media only screen and (max-width: 768px) {
  .articles {
    padding: 40px 20px;
  }
}
</style>
