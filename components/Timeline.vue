<template>
  <section>
    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <strong>{{ experience.title }}</strong>
      <p>{{ experience.content }}</p>
    </div>
  </section>
</template>

<style scoped>

.experience {
  position: relative;
  padding-top: 10px;
  padding-left: 30px;
  padding-bottom: 20px;
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
  props: {
    experiences: {
      type: Array,
    }
  }
}
</script>
