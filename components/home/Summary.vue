<template>
  <section>
    <Intro>
      Hello! Thanks for visiting my page. I’m {{ nickname }}. I’m as aspiring
      software professional living in Edmonton, Alberta. While my primary
      insterest is in backend and networking, I do a little bit of front-end
      work, such as this.
      <br />
      <br />
      Right now I am pursuing Masters in Information Systems Security at
      Concordia University, Montreal. While that might be little surprising
      given my location, in this remote world nothing is impossible!
    </Intro>
  </section>
</template>

<script>
export default {
  data() {
    var nickname = "Rafee";
    return {
      nickname,
    };
  },
};
</script>
