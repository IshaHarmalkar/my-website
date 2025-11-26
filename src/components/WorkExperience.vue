<template>
  <q-section class="q-pa-md bg-grey-1">
    <div class="text-h3 text-primary q-mb-lg">👩🏽‍💻 Internships</div>

    <div class="row q-col-gutter-md">
      <div v-for="(job, index) in experiences" :key="index" class="col-12 col-sm-6 col-md-4">
        <q-card flat bordered class="q-pa-md my-card">
          <div class="row items-center q-gutter-sm">
            <q-avatar size="56px" rounded v-if="job.logo">
              <img :src="job.logo" :alt="job.company" />
            </q-avatar>

            <div class="column">
              <div class="text-h6">{{ job.role }}</div>
              <div class="text-subtitle2 text-grey-7">{{ job.company }}</div>
              <div class="text-caption text-grey-6">{{ job.duration }}</div>
            </div>
          </div>

          <q-separator spaced />

          <ul class="q-pl-md">
            <li v-for="(point, i) in job.responsibilities" :key="i" class="text-body2">
              {{ point }}
            </li>
          </ul>
        </q-card>
      </div>
    </div>
  </q-section>
</template>

<script>
export default {
  name: 'WorkExperience',
  data() {
    return {
      experiences: [
        {
          role: 'Software Developer Intern',

          company: 'Splintly',
          duration: 'Sep 2025 – Nov 2025',
          logo: '/icons/spintly.png',
          responsibilities: [
            'Designing and building microservices with golang and Apache Kakfa on the Integrations team',
            'Golang REST apis, kafka producer consumers, Postgress, mermaid flow diagrams',
            'Owned the process from system design to writing code to production.',
          ],
        },
        {
          role: 'Software Developer Intern',
          company: 'CVSynk.',
          duration: 'Jan 2025 – March 2025',
          logo: '/icons/cv-synk.svg',
          responsibilities: [
            'Developed full-stack hiring automation application using Laravel, Vue.js Composition API, Quasar, Pinia, and MySQL',
            ' Built modules with RESTful APIs,  Eloquent  model relations for clean db interactions. ',
            'Implemented secure authentication with role based authentication with Sanctum, file upload with storage facade',
          ],
        },
        {
          role: 'Software Developer Intern',
          company: 'AppBuddy LLP',
          duration: 'Jun 2024 – Aug 2024',
          logo: '/icons/app-buddy.png',
          responsibilities: [
            'Worked with Node js and vue js, MVC architecture. Mongodb for database',
            'Developed a realtime weather app, refactored web pages for seo, web crawlers',
            'Worked with google web master for resolving issues.',
          ],
        },
      ],
    }
  },
}
</script>

<style scoped>
ul {
  margin: 0;
}

.my-card {
  min-height: 300px;
  padding: 20px;
}
</style>
