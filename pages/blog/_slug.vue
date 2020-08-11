<template>
  <section>
    <section class="go-back">
      <nuxt-link to="/blog" class="articles-link">
        <i class="material-icons">keyboard_backspace</i> Retour aux articles
      </nuxt-link>
    </section>

    <article>
      <nuxt-content :document="article" />
    </article>
  </section>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  },
}
</script>

<style scoped>
article {
  padding: 60px 40px;
  background-color: var(--white);
}

.go-back {
  padding: 40px;
  background-color: var(--white);
  border-bottom: 1px solid var(--yellow);
}

.articles-link {
  display: flex;
  align-items: center;
  text-decoration: none;
  color: black;
  font-size: 20px;
  transition: color .3s;
}

.articles-link > i {
  margin-right: 20px;
}

.articles-link:hover {
  color: var(--yellow);
}
</style>
