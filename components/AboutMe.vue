<template>
  <section class="about-me">
    <h2 class="blue">About me</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil soluta, dolor, maxime sit necessitatibus facere possimus distinctio atque eos quidem doloremque iure.</p>

    <div class="qualities">
      <div class="quality">
        <i class="material-icons md-36 yellow">spa</i>
        <div class="quality-content">
          <h3 class="yellow">Curious</h3>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Et tempore non, sit id minima veniam! Quasi, commodi impedit necessitatibus</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36 green">favorite</i>
        <div class="quality-content">
          <h3 class="green">Passionate</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ea, qui eos illo ipsum cumque nemo temporibus quibusdam laborum possimus</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36 red">camera</i>
        <div class="quality-content">
          <h3 class="red">Meticulous</h3>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quaerat perferendis molestias a dolor dicta accusantium eum, eius tenetur</p>
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
