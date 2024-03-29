<template>
  <section class="experiences">

    <div v-for="experience in experiences" :key="experience.title" class="experience">
      <ExperienceCard
        :company="experience.company"
        :period="experience.period"
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

.experiences:before, .experiences:after {
  content: '';
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

.experience:before, .experience:after {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  content: '';
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

  .experiences:before, .experiences:after {
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

  .experience:before, .experience:after {
    position: absolute;
    left: 50px;
    content: '';
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
import ExperienceCard from "~/components/work/ExperienceCard.vue";

export default {
  components: {
    ExperienceCard,
  },
  data: () => {
    const experiences = [
      {
        company: 'RCA',
        period: '09/2021 - now',
        role: 'Full stack lead developer',
        description: 'Leading a team working on "MEG", an application for accountants and their clients allowing them to help them manage their accounts. Developing new functionalities, helping people grow on my team, managing developement practices, handling technical debt like removing Angular.js bit by bit for example 😅',
        skills: [
          'Angular.js', 'Angular', 'Javascript', 'Typescript', 'Css', 'Java', 'Spring boot', 'Kafka', 'Postgresql'
        ]
      },
      {
        company: 'Digitemis',
        period: '03/2021 - 08/2021',
        role: 'JS lead developer',
        description: 'Worked on "Make It Safe", a security repository platform allowing the analysis, entry and sharing of audits on various security subjects. I helped introduced developement best practices, reworked the git process, handled technical debt on the Vue.js and CSS code and developed new functionalities while helping people on the team grow their skills.',
        skills: [
          'Vue.js', 'Git', 'Javascript', 'Css'
        ]
      },
      {
        company: 'My Money Bank',
        period: '01/2020 - 02/2021',
        role: 'JS lead developer',
        description: 'Leading a team of 2 developers (+ me) on the JS part of an application handling the creation and management of credits in a bank. JS part meaning React + node.js server. Introducing best practices, handling technical debt, developing people technical and soft skills.',
        skills: [
          'React', 'Node.js', 'Typescript', 'Graphql', 'Sentry', 'Cypress', 'Codecept', 'Java', 'Spring boot',
        ]
      },
      {
        company: 'My Money Bank',
        period: '11/2018 - 12/2019',
        role: 'Full stack developer',
        description: 'Development of an application to create and manage credits. We acquire, verify and save clients data like the financial situation, official documents, requirement and so on. We also calculate indicators from this data to help decision making. Front end was made with React. The back-end are micro-services developed in Java with Spring boot, and to connect both part we have a graphql server developed in Node.js and Typescript.',
        skills: [
          'React', 'Node.js', 'Typescript', 'Graphql', 'Cypress', 'Codecept', 'Java', 'Spring boot'
        ]
      },
      {
        company: 'Saint-Gobain',
        period: '03/2018 - 10/2018',
        role: 'Full stack developer',
        description: 'Development of an application to handle business logic of a materials manager : purchase, sale, inventory management, etc. The front-end was a big Angular (v5) application divided with a DDD approach into modules. The back-end was a list of REST apis in micro-services made with Java and Spring boot.',
        skills: [
          'Angular', 'Typescript', 'Java', 'Spring boot'
        ]
      },
      {
        company: 'AFP',
        period: '11/2016 - 02/2018',
        role: 'Full stack developer',
        description: 'Development of an application allowing both journalists and people to send videos, photos and text. These elements can be sent associated with metadata. They are uploaded, verified and then indexed to be accessible in the AFP information system. Typescript and Angular (v4) was used for the front-end, Java and Spring boot for the back-end.',
        skills: [
          'Angular', 'Typescript', 'Java', 'Spring boot'
        ]
      },
      {
        company: 'EDF R&D',
        period: '10/2016 - 11/2016',
        role: 'Angular.js developer',
        description: 'Development of a data visualizer using Angular.js. The objective was to be able to observe, compare and analyze data from EDF nuclear power plant sites. The application displayed data in several graphic forms and allow users to apply filters to narrow data to a specific set and compare it to another one. Made with Angular.js (1.5) Chart.s and Bootstrap (v3)',
        skills: [
          'Angular.js', 'Chart.js', 'Bootstrap'
        ]
      },
      {
        company: 'University of La Rochelle - IT System Department',
        period: '9/2014 - 9/2016',
        role: 'Full stack developer - apprentice',
        description: 'Development of a open-source collaborative web platform called OAE (Open Academic Environment). This platform allowed users to create, give access and manage content like docs, excels, classes, similarly to google drive, but to universities and colleges. It also allow users to have the platform on their own servers and manage where are kept their datas by themselves. For example I integrated a Jitsi module to allow users to have visio call in real time. Realized with node.js and Javascript.',
        skills: [
          'Javascript', 'Node.js'
        ]
      },
      {
        company: 'Irium France',
        period: '5/2014 - 8/2014',
        role: 'Php developer - trainee',
        description: 'Development of SOAP webservices to enrich functionalities of an ERP, for customers managing agricultural equipment fleets. Made with CakePHP and Foundation as the css framework.',
        skills: [
          'Php', 'CakePHP', 'Foundation'
        ]
      },
    ]

  return {
      experiences
    }
  }
}
</script>
