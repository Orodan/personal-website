<template>
  <section class="professional-experiences">
    <h2>Professional experiences</h2>

    <Timeline title="titre" :experiences="experiences" />
  </section>
</template>

<script>
import Timeline from './Timeline'

export default {
  components: {
    Timeline,
  },
  data: () => {
    const experiences = [
      {
        title: 'My Money Bank',
        content: '11/2018 - Now | JS developer',
      },
      {
        title: 'Saint Gobain',
        content: '01/2018 - 09/2018 | Full stack developer'
      }
    ]

  return {
      experiences
    }
  }
}
</script>

<style scoped>
.professional-experiences {
  padding: 40px;
  color: #eee;
  background-color: var(--purple);
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
  font-weight: 600;
}
</style>
