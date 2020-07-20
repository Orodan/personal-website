<template>
  <div class="skill-diamond">
    <div>Angular</div>
  </div>
</template>

<style scoped>
.skill-diamond {
  height: 120px;
  width: 120px;
  background-color: var(--white);
  transform: rotate(45deg);
  margin: 20px 40px;
  border-radius: 50%;
}

.skill-diamond > div {
  display: flex;
  height: 120px;
  width: 120px;
  justify-content: center;
  align-items: center;
  transform: rotate(-45deg);
}
</style>
