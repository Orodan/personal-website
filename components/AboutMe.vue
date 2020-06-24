<template>
  <section class="about-me">
    <h2 class="blue">About me</h2>
    <p>Here is the section where I sell how many qualities I have. As much as I "love" talking about myself, here is some stuff I consider relevant to know about me.</p>

    <div class="qualities">
      <div class="quality">
        <i class="material-icons md-36 yellow">spa</i>
        <div class="quality-content">
          <h3 class="yellow">Curious</h3>
          <p>I'm a very curious person in everything I do, work included. I like to understand the "how" and "why". It also means I need to have challenges and discover new stuff.</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36 green">favorite</i>
        <div class="quality-content">
          <h3 class="green">Passionate</h3>
          <p>What I do for work is not only a way to get a paycheck. I love being a developer and a trainer and I'm proud of it. It is a passion in which I invest many hours into.</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36 red">camera</i>
        <div class="quality-content">
          <h3 class="red">Meticulous</h3>
          <p>I'm a meticulous person in every aspects of my work. Software quality is not something I consider an option. Every time I'm engage in a project I try my best to make sure the work is done but also done in a right way.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-me {
  background-color: #fff;
  padding: 40px;
  color: black;
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
  font-weight: 600;
}

h3 {
  text-transform: uppercase;
  line-height: 34px;
  margin-bottom: 10px;
}

p {
  margin-bottom: 20px;
}

.qualities {
  display: flex;
}

.quality {
  display: flex;
  margin: 0 20px;
}

.quality:first-child {
  margin-left: 0;
}

.quality:last-child {
  margin-right: 0;
}

i {
  margin-right: 20px;
}
</style>
