<template>
  <section class="personal-info">
    <h2 class="yellow">Personal Info</h2>

    <ul>
      <li><strong>Name:</strong> <span>Mohammad Ishfaque Jahan Rafee</span></li>
      <li><strong>Email:</strong> <span>mij.rafee.1344@gmail.com</span></li>
      <li><strong>City:</strong> <span>Edmonton</span></li>
      <li><strong>Province:</strong> <span>Alberta</span></li>
      <li><strong>Country:</strong> <span>Canada</span></li>
    </ul>
  </section>
</template>

<style scoped>
.personal-info {
  padding: 40px;
  color: var(--white);
  background-color: var(--light-dark);
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
  font-weight: 600;
}

ul {
  position: relative;
  list-style: none;
  padding: 0;
}

li {
  text-align: left;
  margin: 30px 0;
}

li > span {
  position: absolute;
  left: 30%;
}
</style>
