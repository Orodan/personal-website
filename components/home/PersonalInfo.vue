<template>
  <section class="personal-info">
    <h2 class="yellow">Personal Info</h2>

    <ul>
      <li><strong>Name:</strong> <span>Jimmy Kasprzak</span></li>
      <li><strong>Birth date:</strong> <span>10/11/1993</span></li>
      <li><strong>email:</strong> <span>jimmykasprzakpro@gmail.com</span></li>
      <li><strong>City:</strong> <span>Nantes</span></li>
      <li><strong>Country:</strong> <span>France</span></li>
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
  left: 50%;
}
</style>
