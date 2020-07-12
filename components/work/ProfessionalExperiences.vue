<template>
  <section class="experiences">
    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <strong>{{ experience.title }}</strong>
      <p>{{ experience.content }}</p>
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
  left: -5px;
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
  left: 0;
  top: 0;
  background-color: #eee;
  display: inline-block;
  z-index: 0;
}

.experience:nth-child(odd) {
  transform: translateX(-50%);
  text-align: right;
  padding-right: 30px;
  padding-left: 0;
}

.experience:nth-child(odd):before  {
  position: absolute;
  right: -5px;
  content: '';
  height: 11px;
  width: 11px;
  top: 15px;
  background-color: #eee;
  border-radius: 50%;
  display: inline-block;
  z-index: 1;
  left: auto;
}

.experience:nth-child(odd):after {
  position: absolute;
  content: '';
  height: 100%;
  width: 1px;
  right: 0;
  top: 0;
  background-color: #eee;
  display: inline-block;
  z-index: 0;
  left: auto;
}

.experience:first-child:after {
  top: -13px;
  height: 120%;
}

.experience:last-child:after {
  height: 120%;
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
