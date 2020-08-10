<template>
  <footer>
    <section>
      <h3>Download CV</h3>

      <span class="download-link">English</span>
      <span class="download-link">French</span>
    </section>

    <section>
      <h3>Follow me</h3>

      <a class="social-link" href="https://twitter.com/JimmyKasprzak" target="__blank">
        <img class="social-icon" src="~/assets/Twitter_Logo_WhiteOnBlue.png" alt="twitter logo" />
      </a>
      <a class="social-link" href="https://github.com/Orodan" target="__blank">
        <img class="social-icon" src="~/assets/GitHub-Mark-Light-64px.png" alt="github logo" />
      </a>
      <a class="social-link linkedin" href="https://www.linkedin.com/in/jimmy-kasprzak/" target="__blank">
        <img class="social-icon" src="~/assets/LI-In-Bug.png" alt="linkedin logo" />
      </a>
    </section>

    <section class="copyright">
      Made with love by Jimmy kasprzak.
    </section>
    <section class="copyright">
      © 2020 Jimmy Kasprzak
    </section>
  </footer>
</template>

<style scoped>
.social-link {
  display: inline-block;
  height: 35px;
  width: 35px;
  margin-right: 10px;
  cursor: pointer;
}

.linkedin {
  width: 40px;
}

.social-icon {
  width: 100%;
  height: 100%;
}

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
