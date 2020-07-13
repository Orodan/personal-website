<template>
  <div class="experience-card">
    <strong>{{ title }}</strong>
    <p>{{ content }}</p>
  </div>
</template>

<style scoped>
.experience-card {
  padding: 20px;
  border: thin solid var(--white);
  border-radius: 5px;
}

strong {
  display: inline-block;
  margin-bottom: 5px;
}
</style>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    content: {
      type: String,
    }
  }
}
</script>
