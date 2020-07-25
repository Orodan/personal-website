<template>
  <section class="more-intro">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, dolore et. Explicabo at sequi eius numquam veritatis, necessitatibus iste consectetur distinctio sunt eum laborum illo eaque assumenda quo culpa illum!
  </section>
</template>

<script>
export default {
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
  color: #fff;
  font-size: 26px;
  background-color: var(--yellow);
}
</style>
