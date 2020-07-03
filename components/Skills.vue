<template>
  <section class="skills">
    <h2>Skills</h2>

    <section class="skill-list">
      <div class="skill">Javascript</div>
      <div class="skill">Typescript</div>
      <div class="skill">Angular</div>
      <div class="skill">React</div>
      <div class="skill">Vuejs</div>
      <div class="skill">Java</div>
    </section>
  </section>
</template>

<style scoped>
.skills {
  background-color: var(--blue);
  padding: 40px;
  color: #eee;
}

.skill-list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 20px;
  row-gap: 20px;
}

.skill {
  padding: 20px;
  text-transform: uppercase;
  font-weight: 600;
  border-radius: 3px;
  border: thin solid #eee;
  display: inline-block;
  transition: .3s;
  cursor: pointer;
}

.skill:hover {
  background-color: #eee;
  color: var(--blue);
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
  font-weight: 600;
}
</style>
