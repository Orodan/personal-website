<template>
  <section>
    <section class="more-intro">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, dolore et. Explicabo at sequi eius numquam veritatis, necessitatibus iste consectetur distinctio sunt eum laborum illo eaque assumenda quo culpa illum!
    </section>

    <article>
      <nuxt-content :document="article" />
    </article>
  </section>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const article = await $content('articles', 'creating-personal-website-with-nuxt').fetch()

    return { article }
  },
  data () {
    return {
      title: 'Jimmy Kasprzak | more',
    }
  },
  head () {
    return {
      title: this.title,
    }
  }
}
</script>

<style scoped>
.more-intro {
  padding: 60px 40px;
  color: var(--white);
  font-size: 26px;
  background-color: var(--yellow);
}

article {
  padding: 60px 40px;
  background-color: var(--white);
}
</style>
