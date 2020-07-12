<template>
  <section class="experiences">
    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <div class="experience-card">
        <strong>{{ experience.title }}</strong>
        <p>{{ experience.content }}</p>
      </div>
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

.experiences:before {
  content: '';
  border-radius: 50%;
  background-color: #eee;
  width: 25px;
  height: 25px;
  transform: translateY(-50%);
}

.experiences:after {
  content: '';
  border-radius: 50%;
  background-color: #eee;
  width: 25px;
  height: 25px;
  transform: translateY(50%);
}

.experience {
  display: flex;
  justify-content: center;
  position: relative;
  color: #eee;
  width: 100%;
}

.experience:before {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: '';
  height: 11px;
  width: 11px;
  top: 30px;
  background-color: #eee;
  border-radius: 50%;
  z-index: 1;
}

.experience:after {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: '';
  height: 100%;
  width: 1px;
  top: 0;
  background-color: #eee;
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

.experience-card {
  padding: 20px;
}

.experience:nth-child(odd) .experience-card {
  transform: translateX(70%);
}

.experience:nth-child(even) .experience-card {
  transform: translateX(-70%);
  text-align: right;
}
</style>

<script>
export default {
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
