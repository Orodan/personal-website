<template>
  <nav>
    <div class="bg-green">
      <i class="material-icons md-48">home</i>
      <p>Home</p>
    </div>

    <div class="bg-blue">
      <i class="material-icons md-48">emoji_emotions</i>
      <p>About me</p>
    </div>

    <div class="bg-purple">
      <i class="material-icons md-48">work</i>
      <p>Work</p>
    </div>

    <div class="bg-orange">
      <i class="material-icons md-48">star</i>
      <p>Skills</p>
    </div>

    <div class="bg-red">
      <i class="material-icons md-48">share</i>
      <p>Contact</p>
    </div>

    <div class="bg-yellow">
      <i class="material-icons md-48">more</i>
      <p>More</p>
    </div>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
}

nav > div {
  flex: 1;
  height: 100px;
  position: relative;
  display: flex;
  justify-content: center;
  cursor: pointer;
}

nav > div:hover {
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
