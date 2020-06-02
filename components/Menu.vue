<template>
  <nav>
    <div class="green">
      <i class="material-icons md-48">home</i>
      <p>Home</p>
    </div>

    <div class="blue">
      <i class="material-icons md-48">emoji_emotions</i>
      <p>About me</p>
    </div>

    <div class="purple">
      <i class="material-icons md-48">work</i>
      <p>Work</p>
    </div>

    <div class="orange">
      <i class="material-icons md-48">star</i>
      <p>Skills</p>
    </div>

    <div class="red">
      <i class="material-icons md-48">share</i>
      <p>Contact</p>
    </div>

    <div class="yellow">
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
}

i {
  position: absolute;
  top: 16px;
}

p {
  position: absolute;
  bottom: 10px;
}

.green { background-color: #43a047; }
.blue { background-color: #039be5; }
.purple { background-color: #8e24aa; }
.orange { background-color: #fb8c00; }
.red { background-color: #e53935; }
.yellow { background-color: #fbc02d; }

.material-icons.md-18 { font-size: 18px; }
.material-icons.md-24 { font-size: 24px; }
.material-icons.md-36 { font-size: 36px; }
.material-icons.md-48 { font-size: 48px; }
</style>
