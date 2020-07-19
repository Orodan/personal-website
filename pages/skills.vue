<template>
  <section>
    <section class="skills-intro">
      In this page, you can find tech skills I like to use at the moment.
      <br />
      This is non-exhaustive, completly subjective, but it allows you to know very quickly what my tech interests and competences are at the moment.
    </section>

    <section class="diamonds-container">
      <section class="level expert">
        <div class="level-intro">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus placeat enim facilis asperiores nam excepturi adipisci ipsam amet nisi tempora temporibus, magnam eos consectetur facere aliquam debitis dolorem. Totam, similique.
        </div>

        <div class="level-content">
          <SkillDiamond />
          <SkillDiamond />
          <SkillDiamond />
        </div>
      </section>

      <section class="level good">
        <div class="level-intro">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus placeat enim facilis asperiores nam excepturi adipisci ipsam amet nisi tempora temporibus, magnam eos consectetur facere aliquam debitis dolorem. Totam, similique.
        </div>

        <div class="level-content">
          <SkillDiamond />
          <SkillDiamond />
          <SkillDiamond />
        </div>
      </section>

      <section class="level medium">
        <div class="level-intro">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Possimus placeat enim facilis asperiores nam excepturi adipisci ipsam amet nisi tempora temporibus, magnam eos consectetur facere aliquam debitis dolorem. Totam, similique.
        </div>

        <div class="level-content">
          <SkillDiamond />
          <SkillDiamond />
          <SkillDiamond />
        </div>
      </section>
    </section>
  </section>
</template>

<script>
import SkillDiamond from "~/components/skills/SkillDiamond.vue";

export default {
  components: {
    SkillDiamond
  },
  data: () => {
    const skills = [
      {
        title: 'Angular',
        content: 'My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.'
      },
      {
        title: 'Angular',
        content: 'My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.'
      },
      {
        title: 'Angular',
        content: 'My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.'
      },
      {
        title: 'Angular',
        content: 'My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.'
      },
      {
        title: 'Angular',
        content: 'My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.'
      }
    ]

    return {
      skills
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
  align-items: center;
}

.level-content {
  display: flex;
  justify-content: center;
  padding: 40px;
}

.skills-intro {
  padding: 60px 40px;
  color: var(--white);
  font-size: 26px;
  background-color: var(--orange);
}

.skill-list {
  display: flex;
  flex-wrap: wrap;
  background-color: var(--white);
  padding: 40px;
}
</style>
