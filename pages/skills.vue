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
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus placeat enim facilis asperiores nam excepturi adipisci ipsam amet nisi tempora temporibus, magnam eos consectetur facere aliquam debitis dolorem. Totam, similique.
          </p>
        </div>

        <div class="level-content">
          <section>
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
          </section>
          <section>
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
          </section>
        </div>
      </section>

      <section class="level good">
        <div class="level-intro">
          <h3>Good</h3>

          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus placeat enim facilis asperiores nam excepturi adipisci ipsam amet nisi tempora temporibus, magnam eos consectetur facere aliquam debitis dolorem. Totam, similique.
          </p>
        </div>

        <div class="level-content">
          <section>
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
          </section>
          <section>
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
            <SkillCard title="Angular" />
          </section>
        </div>
      </section>

      <section class="soft-skills-intro ">
        Because work is not only about tech skills, below you can also find soft skills I value a lot.
      </section>

      <section class="soft-skills">
        <div class="soft-skill">
          <strong class="orange">Communication</strong>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque sunt cum omnis? Provident officia ut nulla est magnam, rerum ex inventore, voluptate similique fugiat iusto sed repellat odio laboriosam ducimus!</p>
        </div>

        <div class="soft-skill">
          <strong class="green">Empathy</strong>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque sunt cum omnis? Provident officia ut nulla est magnam, rerum ex inventore, voluptate similique fugiat iusto sed repellat odio laboriosam ducimus!</p>
        </div>

        <div class="soft-skill">
          <strong class="blue">Benevolence</strong>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque sunt cum omnis? Provident officia ut nulla est magnam, rerum ex inventore, voluptate similique fugiat iusto sed repellat odio laboriosam ducimus!</p>
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
</style>
