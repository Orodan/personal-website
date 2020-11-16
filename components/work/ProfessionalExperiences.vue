<template>
  <section class="experiences">
    <div
      v-for="experience in experiences"
      :key="experience.title"
      class="experience"
    >
      <ExperienceCard
        :company="experience.company"
        :startTime="experience.startTime"
        :endTime="experience.endTime"
        :role="experience.role"
        :description="experience.description"
        :skills="experience.skills"
      />
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

.experiences:before,
.experiences:after {
  content: "";
  border-radius: 50%;
  background-color: var(--white);
  width: 25px;
  height: 25px;
}

.experience {
  display: flex;
  justify-content: center;
  position: relative;
  color: var(--white);
  width: 100%;
}

.experience:before,
.experience:after {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: "";
}

.experience:before {
  height: 11px;
  width: 11px;
  top: 40px;
  background-color: var(--white);
  border-radius: 50%;
  z-index: 1;
}

.experience:after {
  height: 100%;
  width: 1px;
  top: 0;
  background-color: var(--white);
  z-index: 0;
  display: inline-block;
}

.experience:first-child {
  padding-top: 40px;
}

.experience:last-child {
  padding-bottom: 40px;
}

.experience:nth-child(odd) > * {
  transform: translateX(70%);
}

.experience:nth-child(even) > * {
  transform: translateX(-70%);
  text-align: right;
}

@media only screen and (max-width: 768px) {
  .experiences {
    align-items: normal;
  }

  .experiences:before,
  .experiences:after {
    margin-left: 38px;
  }

  .experience {
    margin: 20px 0;
    justify-content: center;
  }

  .experience:nth-child(odd) > *,
  .experience:nth-child(even) > * {
    transform: translateX(0%);
    text-align: left;
  }

  .experience:before,
  .experience:after {
    position: absolute;
    left: 50px;
    content: "";
  }

  .experience:after {
    height: auto;
    top: -20px;
    bottom: -20px;
  }
}

@media only screen and (max-width: 425px) {
  .experiences:before,
  .experiences:after,
  .experience:before,
  .experience:after {
    display: none;
  }

  .experiences {
    padding: 0;
  }

  .experience {
    padding: 10px;
    margin: 0;
  }

  .experience:first-child {
    padding-top: 20px;
  }

  .experience:last-child {
    padding-bottom: 20px;
  }
}
</style>

<script>
export default {
  data: () => {
    const experiences = [
      {
        company: "Concordia University",
        startTime: new Date(2018, 9),
        endTime: new Date(2020, 10),
        // period: "11/2018 - Now",
        role: "Graduate Research Assistant",
        description: [
          "Developed a video streaming server, which uses native UDP multicast to stream to multiple clients simultaneously over HTTP. The deployment used an experimental variation of QUIC, QUIC multicast, as foundation for HTTP multicast.",
          "Designed experiment to test Go network library for Information Centric Networking. Determined the metrics necessary for testing and comparing the library against other similar libraries written in other programming languages, such as Java, C++ etc.",
        ],
        skills: ["TCP/IP", "Go", "C++", "HTTP", "REST"],
      },
      {
        company: "ZTE Corporation (Bangladesh) Limited",
        startTime: new Date(2017, 11),
        endTime: new Date(2018, 8),
        // period: "11/2018 - Now",
        role: "Technical Account Manager",
        description: [
          "Worked as a technical interface to Key Decision Makers of Bangladesh Government in first Tier-4 Data Center Project in Bangladesh.",
          "Signed deal worth 8M with one of the largest ISP in Bangladesh for GPON and Cloud Infrastructure.",
        ],
        skills: ["Sales", "Customer Support"],
      },
      {
        company: "Huawei Technologies (Bangladesh) Limited",
        startTime: new Date(2014, 9),
        endTime: new Date(2017, 11),
        // period: "11/2018 - Now",
        role: "Solutions Engineer",
        description: [
          "Designed solution for first hosted cloud data center project in Bangladesh. The project launched as a new business line for the customer.",
          "Reduced 5 EMC storage boxes to single high-end Huawei storage decreasing the physical footprint by 80% and power consumption by 50%, resulting in 60% reduction in estimated TCO over five years.",
          "Consolidated forty-two physical rack servers to the first virtualization platform in Teletalk. The consolidation resulted in a close to 90% reduction in physical footprint and 70% power consumption.",
        ],
        skills: [
          "Cloud Computing",
          "Server",
          "Storage",
          "Virtualization",
          "Sales",
        ],
      },
    ];

    return {
      experiences,
    };
  },
};
</script>
