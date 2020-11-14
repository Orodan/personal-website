<template>
  <div class="container">
    <Header />

    <Nuxt />

    <Footer />
  </div>
</template>

<script>
import Header from "~/components/common/Header.vue";
import Footer from "~/components/common/Footer.vue";

export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  color: #2e495e;
}

body {
  background-color: #eee;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  max-width: 1390px;
  margin: 0 auto;
  flex-direction: column;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #00c48d;
  color: #00c48d;
  text-decoration: none;
  padding: 10px 30px;
  display: inline-flex;
  align-self: center;
}

.button--green:hover {
  color: #fff;
  background-color: #00c48d;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #2e495e;
  color: #2e495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #2e495e;
}
</style>
