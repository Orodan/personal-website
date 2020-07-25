<template>
  <section>
    <section class="self-intro">
      Hi, I’m Jimmy. I’m an French software engineer living and working in Nantes, France.
      <br/>
      I'm also a trainer and I love sharing my passion for software development with people in many ways like writing blogs and speaking at meetups and conferences.
    </section>

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/la-rochelle.jpg" alt="la rochelle picture">
      </div>

      <div class="story-content blue">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos quasi iusto obcaecati necessitatibus, blanditiis ex exercitationem? Fugiat tempora consectetur eius quasi minus exercitationem, aspernatur fuga hic laboriosam, praesentium, voluptatibus veritatis.
      </div>
    </section>

    <section class="story">
      <div class="story-content bg-blue white">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos quasi iusto obcaecati necessitatibus, blanditiis ex exercitationem? Fugiat tempora consectetur eius quasi minus exercitationem, aspernatur fuga hic laboriosam, praesentium, voluptatibus veritatis.
      </div>

      <div class="story-picture violet">
        <img src="~/assets/paris.jpeg" alt="paris picture">
      </div>
    </section>

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/nantes.jpg" alt="nantes picture">
      </div>

      <div class="story-content blue">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos quasi iusto obcaecati necessitatibus, blanditiis ex exercitationem? Fugiat tempora consectetur eius quasi minus exercitationem, aspernatur fuga hic laboriosam, praesentium, voluptatibus veritatis.
      </div>
    </section>

    <AboutMe />
  </section>
</template>

<style scoped>
.self-intro {
  padding: 60px 40px;
  color: #fff;
  font-size: 26px;
  background-color: var(--blue);
}

.story {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  color: black;
  background-color: #fff;
}

.story-picture {
  display: flex;
}

.story-content {
  display: flex;
  padding: 40px;
  font-size: 26px;
  align-items: center;
  justify-content: center;
}

img {
  max-width: 695px;
}
</style>

<script>
import AboutMe from "~/components/AboutMe.vue";

export default {
  components: {
    AboutMe,
  },
  data () {
    return {
      title: 'Jimmy Kasprzak | about me',
    }
  },
  head () {
    return {
      title: this.title,
    }
  }
};
</script>
