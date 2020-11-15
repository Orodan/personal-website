<template>
  <section>
    <Summary :class="'white bg-blue'" />

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/la-rochelle.jpg" alt="la rochelle picture" />
      </div>

      <div class="story-content blue">
        My story started in the beautiful city of La Rochelle. I joined the
        computer science university where I studied for five years to get my
        master degree. In the last two years, I had the chance to be an
        apprentice in the information system management of my university.
      </div>
    </section>

    <section class="story">
      <div class="story-content bg-blue white">
        After getting my master degree, I decided to leave La Rochelle and try
        my luck in Paris where I chose to join Zenika. I stayed for 2 years
        where I got to work for EDF, AFP and Saint-Gobain, meeting amazing
        people and developping my skills in web development, mostly on
        Javascript, Angular and Spring. I also became a trainer and gave
        formations on web topics.
      </div>

      <div class="story-picture violet">
        <img src="~/assets/paris.jpeg" alt="paris picture" />
      </div>
    </section>

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/nantes.jpg" alt="nantes picture" />
      </div>

      <div class="story-content blue">
        Finally, I moved from Paris to Nantes. Luckily Zenika already had an
        agency where I could continue my journey in. Since I got here, I've been
        working as a web developer for MMB where I learned React, graphql and so
        much more thanks to the people around me. And my journey keeps going
        until today in this beautiful city ...
      </div>
    </section>
  </section>
</template>

<script>
export default {
  data() {
    var name = "Mohammad Ishfaque Jahan Rafee";
    var nickname = "Rafee";
    return {
      nickname,
      title: name + " | about me",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>

<style scoped>
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

@media only screen and (max-width: 768px) {
  .story-content {
    font-size: 24px;
  }

  img {
    max-width: 100%;
    object-fit: cover;
  }
}

@media only screen and (max-width: 425px) {
  img {
    display: none;
  }

  .story {
    display: block;
  }
}
</style>
