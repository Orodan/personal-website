<template>
  <section class="experiences">
    <div v-for="experience in experiences" :key="experience.title">
      <div class="experience">
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
  background-color: var(--purple)
}

.experience {
  position: relative;
  padding-top: 10px;
  padding-left: 30px;
  padding-bottom: 20px;
  transform: translateX(50%);
  color: #eee;
}

.experience:before {
  position: absolute;
  content: '';
  height: 11px;
  width: 11px;
  left: 5px;
  top: 15px;
  background-color: #eee;
  border-radius: 50%;
  display: inline-block;
  z-index: 1;
}

.experience:after {
  position: absolute;
  content: '';
  height: 100%;
  width: 1px;
  left: 10px;
  top: 0;
  background-color: #eee;
  display: inline-block;
  z-index: 0;
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
      }
    ]

  return {
      experiences
    }
  }
}
</script>
