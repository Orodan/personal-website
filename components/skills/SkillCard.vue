<template>
  <div class="skill-card">
    <div>{{ title }}</div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String
    }
  }
}
</script>

<style scoped>
.skill-card {
  height: 120px;
  width: 120px;
  background-color: var(--white);
  margin: 20px 40px;
  border-radius: 50%;
}

.skill-card > div {
  display: flex;
  height: 120px;
  width: 120px;
  justify-content: center;
  align-items: center;
}
</style>
