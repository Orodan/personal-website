<template>
  <section class="about-me">
    <h2>About me</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui saepe rem temporibus facere laudantium commodi voluptates mollitia reprehenderit nisi autem? Exercitationem optio architecto assumenda cum consequuntur praesentium rem atque itaque.</p>

    <div class="qualities">
      <div class="quality">
        <i class="material-icons md-36">home</i>
        <div class="quality-content">
          <h3>Creative</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit tenetur dolor, minima accusamus error est at natus velit eveniet! Cupiditate est maxime aspernatur numquam quos minima dolore rerum delectus doloremque?</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36">home</i>
        <div class="quality-content">
          <h3>Creative</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit tenetur dolor, minima accusamus error est at natus velit eveniet! Cupiditate est maxime aspernatur numquam quos minima dolore rerum delectus doloremque?</p>
        </div>
      </div>

      <div class="quality">
        <i class="material-icons md-36">home</i>
        <div class="quality-content">
          <h3>Creative</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit tenetur dolor, minima accusamus error est at natus velit eveniet! Cupiditate est maxime aspernatur numquam quos minima dolore rerum delectus doloremque?</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-me {
  background-color: #fff;
  padding: 40px;
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
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
  color: red;
}
</style>
