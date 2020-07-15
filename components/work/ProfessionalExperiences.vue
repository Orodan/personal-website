<template>
  <section class="experiences">

    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <ExperienceCard
        :company="experience.company"
        :period="experience.period"
        :role="experience.role"
        :description="experience.description"
        :skills="experience.skills"
      />
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
  top: 40px;
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

.experience:first-child {
  padding-top: 40px;
}

.experience:last-child {
  padding-bottom: 40px;
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
        company: 'My Money Bank',
        period: '11/2018 - Now',
        role: 'JS developer',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas totam incidunt ipsam, reprehenderit asperiores eaque, inventore minima quisquam voluptatem exercitationem recusandae assumenda nam',
        skills: [
          'React', 'Node.js', 'Graphql'
        ]
      },
      {
        company: 'My Money Bank 2',
        period: '11/2018 - Now',
        role: 'JS developer',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas totam incidunt ipsam, reprehenderit asperiores eaque, inventore minima quisquam voluptatem exercitationem recusandae assumenda nam',
        skills: [
          'React', 'Node.js', 'Graphql'
        ]
      },
      {
        company: 'My Money Bank 3',
        period: '11/2018 - Now',
        role: 'JS developer',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas totam incidunt ipsam, reprehenderit asperiores eaque, inventore minima quisquam voluptatem exercitationem recusandae assumenda nam',
        skills: [
          'React', 'Node.js', 'Graphql'
        ]
      },
      {
        company: 'My Money Bank 4',
        period: '11/2018 - Now',
        role: 'JS developer',
        description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas totam incidunt ipsam, reprehenderit asperiores eaque, inventore minima quisquam voluptatem exercitationem recusandae assumenda nam',
        skills: [
          'React', 'Node.js', 'Graphql'
        ]
      },
    ]

  return {
      experiences
    }
  }
}
</script>
