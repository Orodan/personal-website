<template>
  <section>
    <section class="skills-intro">
      In this page, you can find skills (both tech and soft) I like to use at the moment.
      <br />
      This is non-exhaustive, completly subjective, but it allows you to know very quickly what my tech interests and competences are at the moment. If you want more details on my experience
      on the listed skills, check out my work page :).
    </section>

    <section class="diamonds-container">
      <section class="level expert">
        <div class="level-intro">
          <h3>Proficient</h3>

          <p>
          On this section you can find skills I'm proficient at. It basically means I can hold my own when working with these technologies. I can manage and lead projects made with them and teach about it to others (I actually do teach about them already).
          </p>
        </div>

        <div class="level-content">
          <section>
            <SkillCard title="JS" />
            <SkillCard title="Node.js" />
            <SkillCard title="Angular" />
          </section>
          <section>
            <SkillCard title="React" />
            <SkillCard title="Graphql" />
            <SkillCard title="Typescript" />
          </section>
        </div>
      </section>

      <section class="level good">
        <div class="level-content">
          <section>
            <SkillCard title="Java" />
            <SkillCard title="Spring" />
            <SkillCard title="Vue.js" />
          </section>
          <section>
            <SkillCard title="Nuxt" />
            <SkillCard title="Rxjs" />
            <SkillCard title="Css" />
          </section>
        </div>

        <div class="level-intro">
          <h3>Good</h3>

          <p>
            You'll find on this section technologies I'm used to work with. I'm no expert but I still considered myself good enough on those to be productive when developing with them.
          </p>
        </div>
      </section>

      <section class="soft-skills-intro">
        Because work is not only about tech skills, below you can also find soft skills I value a lot.
      </section>

      <section class="soft-skills">
        <div class="soft-skill">
          <strong class="orange">Communication</strong>
          <p>No matter the company, the technologie or the people you're working with, communication is for me an essential skill in every project. A project never gets done alone. Being skilled technicaly is good, but being able to communicate and explain what you did to the people around you is even better !</p>
        </div>

        <div class="soft-skill">
          <strong class="green">Empathy</strong>
          <p>Empathy is usefull in some many ways when working, even as a developer. It allows you to properly comprehend what the user wants. It allows you to explain what's wrong in a code review without hurting your colleague. It allows you to comunicate properly to non-tech people. Etc ... Empathy is essential :)</p>
        </div>

        <div class="soft-skill">
          <strong class="blue">Benevolence</strong>
          <p>Always consider that everyone is doing his best in their work. You will always encounter problems when working, but almost nobody come working with the intention to mess up something. Consider other people with benevolence and they will do the same with you.</p>
        </div>
      </section>
    </section>
  </section>
</template>

<script>
import SkillCard from "~/components/skills/SkillCard.vue";

export default {
  components: {
    SkillCard
  },
  data: () => {
    return {
      title: 'Jimmy Kasprzak | skills'
    }
  },
  head () {
    return {
      title: this.title
    }
  }
}
</script>

<style scoped>
.level {
  display: flex;
  padding: 40px;
  justify-content: center;
}

.expert {
  background-color: var(--green);
}

.good {
  background-color: #67cc6b;
}

.medium {
  background-color: var(--orange);
}

.level-intro {
  padding: 40px;
  color: var(--white);
  font-size: 18px;
  display: flex;
  flex-direction: column;
}

.level-intro h3 {
  font-size: 26px;
  flex: 1;
}

.level-intro > p {
  flex: 2;
}

.level-content {
  display: flex;
  justify-content: center;
  padding: 40px;
  flex-direction: column;
}

.level-content > section {
  display: flex;
}

.skills-intro {
  padding: 60px 40px;
  font-size: 24px;
  background-color: var(--white);
}

.soft-skills-intro {
  padding: 60px 40px 40px 40px;
  font-size: 24px;
  background-color: var(--white);
}

.skill-list {
  display: flex;
  flex-wrap: wrap;
  background-color: var(--white);
  padding: 40px;
}

.soft-skills {
  padding: 0 40px 60px 40px;
  display: flex;
  background-color: var(--white);
}

.soft-skill {
  margin-right: 30px;
}

.soft-skill > strong {
  font-size: 22px;
}

.soft-skill > p {
  margin-top: 20px;
}

@media only screen and (max-width: 768px) {
  .level {
    flex-direction: column;
    padding: 20px;
  }

  .level h3 {
    margin-bottom: 20px;
  }

  .level.good {
    flex-direction: column-reverse;
  }

  .level-content {
    overflow-x: hidden;
    flex-wrap: wrap;
    padding: 0;
  }

  .level-content > section {
    justify-content: center;
    flex-wrap: wrap;
  }
}

@media only screen and (max-width: 425px) {
  .level-intro {
    padding: 20px;
  }

  .soft-skills-intro {
    padding: 40px;
  }

  .soft-skills {
    flex-wrap: wrap;
    padding: 0 40px 40px 40px;
  }

  .soft-skill {
    margin-right: 0;
  }

  .soft-skill > p {
    margin-bottom: 20px;
  }

  .soft-skill:last-child > p {
    margin-bottom: 0;
  }
}
</style>
