<template>
  <section class="professional-experiences-summary">
    <h2>Professional experiences</h2>

    <Timeline title="titre" :experiences="experiences" />
  </section>
</template>

<script>
import Timeline from "./Timeline";

export default {
  components: {
    Timeline,
  },
  data: () => {
    const experiences = [
      {
        title: "Concordia University, Montreal, QC",
        content: "09/2018 - 10/2020 | Graduate Research Assistant",
      },
      {
        title: "ZTE Corporation (Bangladesh) Limited",
        content: "11/2017 - 08/2018 | Technical Account Manager",
      },
      {
        title: "Huawei Technologies (Bangladesh) Limited",
        content: "09/2014 - 11/2017 | Solutions Engineer",
      },
    ];

    return {
      experiences,
    };
  },
};
</script>

<style scoped>
.professional-experiences-summary {
  padding: 40px;
  color: #eee;
  background-color: var(--purple);
}

h2 {
  text-transform: uppercase;
  margin-bottom: 20px;
  font-weight: 600;
}
</style>
