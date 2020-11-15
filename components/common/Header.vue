<template>
  <header>
    <img src="~/assets/me.jpg" alt="profile picture" />

    <section class="titles">
      <h1>{{ name }}</h1>
      <h2>{{ role }}</h2>
      <Menu />
    </section>
  </header>
</template>

<script>
// import Menu from "~/components/common/Menu.vue";

export default {
  // components: {
  //   Menu,
  // },
  data() {
    return {
      name: "Mohammad Ishfaque Jahan Rafee",
      role: "Network and Web developer",
    };
  },
};
</script>

<style scoped>
header {
  display: flex;
  color: var(--white);
}

img {
  width: 300px;
  height: 300px;
  object-fit: cover;
}

.titles {
  display: flex;
  flex-direction: column;
  flex: 2;
}

h1,
h2 {
  margin: 0;
  padding: 0 40px;
  font-size: 18px;
  height: 100px;
  line-height: 100px;
  text-transform: uppercase;
}

h1 {
  font-size: 26px;
  background-color: var(--gray);
}

h2 {
  font-size: 24px;
  background-color: var(--dark);
}

@media only screen and (max-width: 768px) {
  header {
    display: block;
  }

  img {
    position: absolute;
    width: 200px;
    height: 200px;
  }

  h1,
  h2 {
    margin-left: 200px;
  }
}

@media only screen and (max-width: 425px) {
  img {
    display: none;
  }

  h1,
  h2 {
    margin-left: 0px;
    height: 70px;
    line-height: 70px;
  }
}
</style>
