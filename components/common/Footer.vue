<template>
  <footer>
    <section class="social-medias">
      <h3>Follow me</h3>

      <a
        class="social-link"
        href="https://twitter.com/JimmyKasprzak"
        target="__blank"
      >
        <img
          class="social-icon"
          src="~/assets/Twitter_Logo_WhiteOnBlue.png"
          alt="twitter logo"
        />
      </a>
      <a class="social-link" href="https://github.com/Orodan" target="__blank">
        <img
          class="social-icon"
          src="~/assets/GitHub-Mark-Light-64px.png"
          alt="github logo"
        />
      </a>
      <a
        class="social-link linkedin"
        href="https://www.linkedin.com/in/jimmy-kasprzak/"
        target="__blank"
      >
        <img
          class="social-icon"
          src="~/assets/LI-In-Bug.png"
          alt="linkedin logo"
        />
      </a>
    </section>
    <section class="copyright">
      © 2020 Jimmy Kasprzak - Made with love by Jimmy kasprzak.
    </section>
  </footer>
</template>

<style scoped>
.social-link {
  display: inline-block;
  height: 35px;
  width: 35px;
  margin-right: 20px;
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
  display: flex;
  flex-direction: column;
  background-color: var(--light-dark);
  color: var(--white);
  padding: 40px;
}

.social-medias {
  margin-bottom: 20px;
}

h3 {
  text-transform: uppercase;
  margin-bottom: 20px;
}

.material-icons {
  margin-right: 10px;
}

.copyright {
  font-size: 18px;
}

@media only screen and (max-width: 425px) {
  footer {
    display: flex;
    flex-direction: column;
  }

  h3 {
    margin-bottom: 20px;
  }
}
</style>
