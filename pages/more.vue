<template>
  <section>
    <section class="more-intro">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, dolore et. Explicabo at sequi eius numquam veritatis, necessitatibus iste consectetur distinctio sunt eum laborum illo eaque assumenda quo culpa illum!
    </section>

    <section class="articles">
      <div class="card-article">
        <h3>Creating my personel website with Nuxt</h3>
        <img src="~/assets/nuxt-icon.png" alt="nuxt icon" />
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate quae sequi amet possimus adipisci ea a ipsa! Ullam atque architecto sint laudantium? Voluptate esse</p>
      </div>
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

.articles {
  display: flex;
  padding: 60px 40px;
  background-color: var(--white);
}

.card-article {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.3);
  border-radius: 5px;
  margin: 20px;
  width: 320px;
  cursor: pointer;
  transition: box-shadow .3s;
}

.card-article:hover {
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.8);
}

.card-article h3 {
  margin-bottom: 20px;
}

.card-article img {
  width: 100%;
  margin-bottom: 20px;
}

article {
  padding: 60px 40px;
  background-color: var(--white);
}
</style>
