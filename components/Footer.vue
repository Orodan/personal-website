<template>
  <footer>
    <section>
      <h3>Download CV</h3>

      <span class="download-link">English</span>
      <span class="download-link">French</span>
    </section>

    <section>
      <h3>Follow me</h3>

      <i class="material-icons">sentiment_satisfied_alt</i>
      <i class="material-icons">sentiment_satisfied_alt</i>
      <i class="material-icons">sentiment_satisfied_alt</i>
      <i class="material-icons">sentiment_satisfied_alt</i>
      <i class="material-icons">sentiment_satisfied_alt</i>
    </section>

    <section class="copyright">© 2020 Jimmy Kasprzak.</section>
  </footer>
</template>

<style scoped>
footer {
  display: grid;
  background-color: #4f4f4f;
  color: #fff;
  padding: 40px;
  grid-template-columns: repeat(2, 1fr);
  row-gap: 40px;
}

h3 {
  text-transform: uppercase;
  margin-bottom: 40px;
}

.download-link {
  padding: 10px 20px;
  border-radius: 3px;
  background-color: #7f7f7f;
  color: #efefef;
  margin-right: 10px;
  cursor: pointer;
  transition: .3s;
}

.download-link:hover {
  background-color: var(--blue);
}

.material-icons {
  margin-right: 10px;
}

.copyright {
  font-size: 18px;
}
</style>
