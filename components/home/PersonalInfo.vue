<template>
  <section class="personal-info">
    <h2 class="yellow">Personal Info</h2>

    <ul>
      <li>
        <strong>Name:</strong> <span>{{ name }}</span>
      </li>
      <li>
        <strong>Email:</strong> <span>{{ email }}</span>
      </li>
      <li>
        <strong>City:</strong> <span>{{ city }}</span>
      </li>
      <li>
        <strong>Province:</strong> <span>{{ province }}</span>
      </li>
      <li>
        <strong>Country:</strong> <span>{{ country }}</span>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data: () => {
    return {
      name: "Mohammad Ishfaque Jahan Rafee",
      email: "mij.rafee.1344@gmail.com",
      city: "Edmonton",
      province: "Alberta",
      country: "Canada",
    };
  },
};
</script>

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
