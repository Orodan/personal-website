<template>
  <nav :class="{ 'sticky': scrolledDown }" ref="navbar">
    <nuxt-link to="/" class="bg-green">
      <i class="material-icons md-48">home</i>
      <p>Home</p>
    </nuxt-link>

    <nuxt-link to="/about-me" class="bg-blue">
      <i class="material-icons md-48">emoji_emotions</i>
      <p>About me</p>
    </nuxt-link>

    <nuxt-link to="/work" class="bg-purple">
      <i class="material-icons md-48">work</i>
      <p>Work</p>
    </nuxt-link>

    <nuxt-link to="/skills" class="bg-orange">
      <i class="material-icons md-48">star</i>
      <p>Skills</p>
    </nuxt-link>

    <nuxt-link to="/contact" class="bg-red">
      <i class="material-icons md-48">share</i>
      <p>Contact</p>
    </nuxt-link>

    <nuxt-link to="/blog" class="bg-yellow">
      <i class="material-icons md-48">article</i>
      <p>Blog</p>
    </nuxt-link>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      scrolledDown: false
    }
  },
  mounted() {
    const navbarOffsetTop = this.$refs.navbar.offsetTop

    window.onscroll = () => {
      this.scrolledDown = window.pageYOffset >= navbarOffsetTop
    }
  }
}
</script>

<style scoped>
nav {
  display: flex;
  z-index: 2;
}

nav > * {
  user-select: none;
  flex: 1;
  height: 100px;
  position: relative;
  display: flex;
  justify-content: center;
  color: #eee;
}

nav > *:hover {
  opacity: .7;
}

i {
  position: absolute;
  top: 16px;
}

p {
  position: absolute;
  bottom: 10px;
}

@media only screen and (max-width: 425px) {
  nav > * {
    height: 70px;
  }

  i.material-icons {
    font-size: 32px;
    top: 10px;
  }

  p {
    font-size: 10px;
  }

  .sticky {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
  }
}
</style>
