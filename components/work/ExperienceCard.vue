<template>
  <div class="experience-card">
    <strong>{{ company }}</strong>
    <p>
      {{
        `${startTime.getMonth()}/${startTime.getFullYear()} - ${endTime.getMonth()}/${endTime.getFullYear()}`
      }}
      | {{ role }}
    </p>

    <ul id="description">
      <li v-for="item in description" :key="item">
        {{ item }}
      </li>
    </ul>

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
      required: true,
    },
    startTime: {
      type: Date,
      required: true,
    },
    endTime: {
      type: Date,
      required: true,
    },
    role: {
      type: String,
      required: true,
    },
    description: {
      type: Array,
      required: true,
    },
    skills: {
      type: Array,
      required: true,
    },
  },
};
</script>
