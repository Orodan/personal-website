<template>
  <section class="skills">
    <h2>Skills</h2>

    <section class="skill-list-container">
      <section class="skill-list">
        <div class="skill">C++</div>
        <div class="skill">Go</div>
        <div class="skill">Java</div>
        <div class="skill">TypeScript</div>
        <div class="skill">Python</div>
        <div class="skill">Vuejs</div>
      </section>
    </section>
  </section>
</template>

<style scoped>
.skills {
  background-color: var(--blue);
  padding: 40px;
  color: #eee;
  display: flex;
  flex-direction: column;
}

.skill-list-container {
  display: flex;
  flex-direction: column;
  flex: 1;
  justify-content: center;
}

.skill-list {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 20px;
  row-gap: 20px;
  width: 100%;
}

.skill {
  padding: 20px;
  text-transform: uppercase;
  font-weight: 600;
  border-radius: 3px;
  border: thin solid #eee;
  display: inline-block;
  transition: 0.3s;
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

@media only screen and (max-width: 425px) {
  .skill-list {
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 15px;
    grid-row-gap: 15px;
  }

  .skill {
    padding: 15px;
  }
}
</style>
