<template>
  <section>
    <Summary :class="'white bg-blue'" />

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/BUET.jpg" alt="la rochelle picture" />
      </div>

      <div class="story-content blue">
        My story started in Bangladesh, a small country in South Asia with
        massive potential. From my childhood, I was fascinated by science and
        math. This fascination brought me to study engineering in the best
        engineering institution in Bangladesh, BUET.
      </div>
    </section>

    <section class="story">
      <div class="story-content bg-blue white">
        After graduation, I first worked as a pre-sales engineer. In that
        position, I had to communicate with all levels of customers. Some of my
        customers had years of technical experience. They were concerned with
        the minute technical details of the solutions. At the same time, CXO
        level customers were more concerned with the business impact. These
        experiences let me develop my technical and non-technical abilities
        simultaneously.
      </div>

      <div class="story-picture violet">
        <img src="~/assets/Huawei.png" alt="paris picture" />
      </div>
    </section>

    <section class="story">
      <div class="story-picture">
        <img src="~/assets/ZTE.jpg" alt="nantes picture" />
      </div>

      <div class="story-content blue">
        Following that, I switched over to a more sales-oriented role. There, I
        got the opportunity to work on a large project (near USD 200M). This
        project had lots of moving parts, which required constant monitoring.
        Due to the size of the project, my impact was nominal. However, it was a
        humbling experience.
      </div>
    </section>

    <section class="story">
      <div class="story-content bg-blue white">
        Now I am studying for MEng at the Information Systems Security at
        Concordia University. While this may seem unconventional (following my
        experience), it's a continuation of my enthusiasm for Cloud Computing
        and Networks. In addition to academics, I have experience with AWS
        (Amazon Web services) and GCP (Google Cloud Platform). I am an AWS
        Certified Cloud Solution Architect - Associate and Google Cloud
        Certified Associate Cloud Engineer.
      </div>

      <div class="story-picture">
        <img src="~/assets/Concordia.jpg" alt="nantes picture" />
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
