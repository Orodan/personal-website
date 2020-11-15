<template>
  <section class="professional-experiences-summary">
    <h2>Professional experiences</h2>

    <Timeline title="title" :experiences="experiences" />
  </section>
</template>

<script>
import Timeline from "./Timeline";
// import Experiences from "../common/Experiences";

export default {
  components: {
    Timeline,
  },
  data: () => {
    const exps = [
      {
        company: "Concordia University",
        location: "Montreal, QC",
        role: "Graduate Research Assistant",
        // Date recorded in YYYY, MM format
        startDate: new Date(2018, 9),
        endDate: new Date(2020, 10),
      },
      {
        company: "ZTE Corporation (Bangladesh) Limited",
        location: "Dhaka",
        role: "Technical Account Manager",
        startDate: new Date(2017, 11),
        endDate: new Date(2018, 8),
      },
      {
        company: "Huawei Technologies (Bangladesh) Limited",
        location: "Dhaka",
        role: "Solutions Engineer",
        startDate: new Date(2014, 9),
        endDate: new Date(2017, 11),
      },
    ];

    var experiences = [];

    // Generate string template from variable data
    for (let index = 0; index < exps.length; index++) {
      const title = `${exps[index].company}, ${exps[index].location}`;
      const content = `${exps[index].startDate.getMonth()}/${exps[
        index
      ].startDate.getFullYear()} - ${exps[index].endDate.getMonth()}/${exps[
        index
      ].endDate.getFullYear()} | ${exps[index].role}`;
      experiences.push({ title: title, content: content });
    }

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
