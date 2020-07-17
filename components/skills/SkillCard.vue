<template>
  <section class="skill-card">
    <div class="skill-card-title">{{ title }}</div>
    <div class="skill-card-content">{{ content }}</div>
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    },
    content: {
      type: String
    }
  }
}
</script>

<style scoped>
.skill-card {
  flex: 1;
  background-color: #eee;
  font-size: 18px;
  margin: 20px;
  border-radius: 3px;
  flex-basis: 350px;
}

.skill-card-title {
  font-size: 26px;
  font-weight: 600;
  background-color: var(--orange);
  color: var(--white);
  padding: 20px 30px;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}

.skill-card-content {
  padding: 30px;
  color: white;
  background-color: #4f4f4f;
}
</style>
