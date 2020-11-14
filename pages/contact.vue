<template>
  <section class="contact">
    <section class="left">
      <img src="~/assets/me.jpg" alt="profile picture" />
    </section>

    <section class="right">
      <ul class="labels">
        <li><strong>Mail:</strong></li>
        <li><strong>Linkedin:</strong></li>
        <li><strong>Github:</strong></li>
      </ul>
      <ul class="values">
        <li>
          <span
            ><a target="__blank" href="mailto:mij.rafee.1344@gmail.com"
              >mij.rafee.1344@gmail.com</a
            ></span
          >
        </li>
        <li>
          <span
            ><a target="__blank" href="https://www.linkedin.com/in/rafee1344"
              >Mohammad Ishfaque Jahan Rafee</a
            ></span
          >
        </li>
        <li>
          <span
            ><a target="__blank" href="https://github.com/rafee">rafee</a></span
          >
        </li>
      </ul>
    </section>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: 'Mohammad Ishfaque Jahan Rafee | contact',
    }
  },
  head() {
    return {
      title: this.title,
    }
  },
}
</script>

<style scoped>
.contact {
  padding: 100px 40px;
  display: flex;
  background: linear-gradient(120deg, var(--white) 50%, var(--red) 50%);
}

.left {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.right {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
}

.right > * {
  flex: 1;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  width: 100%;
  padding: 10px;
}

.labels li {
  text-align: left;
  padding-left: 50%;
}

.values li {
  text-align: left;
}

.right > div:first-child strong {
  text-align: left;
}

strong,
span {
  padding: 10px;
  font-size: 18px;
}

img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  object-fit: cover;
}

a {
  text-decoration: none;
  color: inherit;
}

@media only screen and (max-width: 768px) {
  .contact {
    background: var(--red);
    flex-wrap: wrap;
  }
}

@media only screen and (max-width: 425px) {
  .contact {
    padding: 40px 20px;
  }

  strong,
  span {
    font-size: 14px;
  }

  .right {
    margin-top: 30px;
  }

  .labels li {
    padding-left: 0;
    padding-right: 0;
  }

  .values li {
    padding-left: 0;
    padding-right: 0;
  }
}
</style>
