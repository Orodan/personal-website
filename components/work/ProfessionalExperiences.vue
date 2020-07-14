<template>
  <section class="experiences">

    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <ExperienceCard :title="experience.title" :content="experience.content" />
    </div>
  </section>
</template>

<style scoped>
.experiences {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--purple);
  padding: 40px 0;
  position: relative;
}

.experiences:before, .experiences:after {
  content: '';
  border-radius: 50%;
  background-color: var(--white);
  width: 25px;
  height: 25px;
}

.experiences:before {
  transform: translateY(-50%);
}

.experiences:after {
  transform: translateY(50%);
}

.experience {
  display: flex;
  justify-content: center;
  position: relative;
  color: var(--white);
  width: 100%;
}

.experience:before, .experience:after {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: '';
}

.experience:before {
  height: 11px;
  width: 11px;
  top: 30px;
  background-color: var(--white);
  border-radius: 50%;
  z-index: 1;
}

.experience:after {
  height: 100%;
  width: 1px;
  top: 0;
  background-color: var(--white);
  z-index: 0;
  display: inline-block;
}

.experience:first-child:after {
  top: -13px;
  height: 140%;
}

.experience:last-child:after {
  height: 140%;
}

.experience:nth-child(odd) > * {
  transform: translateX(70%);
}

.experience:nth-child(even) > * {
  transform: translateX(-70%);
  text-align: right;
}
</style>

<script>
import ExperienceCard from "~/components/work/ExperienceCard.vue";

export default {
  components: {
    ExperienceCard,
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
      },
      {
        title: 'My Money Bank',
        content: '11/2018 - Now | JS developer',
      },
      {
        title: 'Saint Gobain',
        content: '01/2018 - 09/2018 | Full stack developer'
      },
    ]

  return {
      experiences
    }
  }
}
</script>
