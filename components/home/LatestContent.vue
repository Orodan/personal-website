<template>
  <section class="about-me">
    <h2 class="blue">Latest content</h2>

    <section class="article-summary" @click="goTo(articleSummary.slug)">
      <div class="article-summary-content">
        <h3 class="green">{{ articleSummary.title }}</h3>
        <p>{{ articleSummary.description }}</p>
      </div>

      <img :src="articleSummary.img" :alt="articleSummary.title" />
    </section>
  </section>
</template>

<script>
export default {
  props: {
    articleSummary: {
      type: Object,
      default: () => ({}),
    },
  },
  methods: {
    goTo: function (slug) {
      this.$router.push({ name: "blog-slug", params: { slug } });
    },
  },
};
</script>

<style scoped>
.about-me {
  background-color: #fff;
  padding: 40px;
  color: black;
}

h2 {
  text-transform: uppercase;
  margin-bottom: 40px;
  font-weight: 600;
}

h3 {
  text-transform: uppercase;
  margin-bottom: 30px;
  font-size: 20px;
  font-weight: 600;
}

p {
  margin-bottom: 20px;
  font-size: 16px;
  flex: 1;
  display: flex;
  align-items: center;
}

img {
  width: 200px;
}

.article-summary {
  display: flex;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.3);
  border-radius: 5px;
  padding: 20px;
  cursor: pointer;
  transition: all 0.3s;
}

.article-summary:hover {
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
}

.article-summary-content {
  display: flex;
  flex-direction: column;
}

@media only screen and (max-width: 425px) {
  img {
    display: none;
  }
}
</style>
