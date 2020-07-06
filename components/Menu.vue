<template>
  <nav>
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

    <nuxt-link to="/more" class="bg-yellow">
      <i class="material-icons md-48">more</i>
      <p>More</p>
    </nuxt-link>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
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

</style>
