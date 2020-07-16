<template>
  <section>
    <section class="skills-intro">
      In this page, you can find tech skills I like to use at the moment.
      <br />
      This is non-exhaustive, completly subjective, but it allows you to know very quickly what my tech interests and competences are at the moment.
    </section>

    <section class="skill-list">
      <div class="skill-card">
        <div class="skill-card-title">Angular</div>
        <div class="skills-card-content">
          My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically
          only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.
        </div>
      </div>

      <div class="skill-card">
        <div class="skill-card-title">Angular</div>
        <div class="skills-card-content">
          My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically
          only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.
        </div>
      </div>

      <div class="skill-card">
        <div class="skill-card-title">Angular</div>
        <div class="skills-card-content">
          My go-to framework/ecosystem by default. I find it very robust, very powerfull and with an awesome documentation and community. You can build an entire real application with basically
          only what Angular provides you and I like the oppinions taken by Angular if you decide to use it on your project.
        </div>
      </div>
    </section>
  </section>
</template>

<style scoped>
.skills-intro {
  padding: 60px 40px;
  color: var(--white);
  font-size: 26px;
  background-color: var(--orange);
}

.skill-list {
  display: flex;
  flex-wrap: wrap;
  background-color: var(--red);
  padding: 40px;
}

.skill-card {
  flex: 1;
  background-color: var(--white);
  padding: 40px;
  font-size: 20px;
  margin: 20px;
}
</style>
