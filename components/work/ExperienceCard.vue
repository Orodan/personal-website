<template>
  <div class="experience-card">
    <strong>{{ company }}</strong>
    <p>{{ period }} | {{ role }}</p>

    <p class="description">{{ description }}</p>
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
    }
  }
}
</script>
