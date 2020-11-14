<template>
  <div class="skill-card">
    <div>{{ title }}</div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped>
.skill-card {
  height: 120px;
  width: 120px;
  background-color: var(--white);
  border-radius: 50%;
}

.skill-card > div {
  display: flex;
  height: 120px;
  width: 120px;
  justify-content: center;
  align-items: center;
}

@media only screen and (max-width: 425px) {
  .skill-card {
    margin: 10px;
  }
}
</style>
