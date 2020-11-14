<template>
  <div class="experience-card">
    <strong>{{ company }}</strong>
    <p>{{ period }} | {{ role }}</p>

    <p class="description">{{ description }}</p>

    <div class="skills">
      <div v-for="skill in skills" :key="skill" class="skill">{{ skill }}</div>
    </div>
  </div>
</template>

<style scoped>
.experience-card {
  padding: 20px;
  border: thin solid var(--white);
  border-radius: 5px;
  max-width: 400px;
}

strong {
  display: inline-block;
  margin-bottom: 5px;
}

.description {
  margin-top: 20px;
}

.skills {
  padding-top: 20px;
}

.skill {
  border: thin solid var(--white);
  border-radius: 3px;
  display: inline-block;
  padding: 10px;
  margin: 10px 10px 0 0;
}

.skill:last-child {
  margin: 10px 0 0;
}
</style>

<script>
export default {
  props: {
    company: {
      type: String,
    },
    period: {
      type: String,
    },
    role: {
      type: String,
    },
    description: {
      type: String,
    },
    skills: {
      type: Array,
    },
  },
};
</script>
