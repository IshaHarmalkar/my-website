<template>
  <div class="container">
    <div class="text-h3 text-primary clean-text">🌻Projects</div>
    <div class="row q-col-gutter-lg q-mt-md">
      <div v-for="(project, index) in projects" :key="index" class="col-12 col-sm-6 col-md-4">
        <q-card class="my-card card-bg" square>
          <img :src="project.img" fit="cover" style="height: 300px" />

          <q-card-section>
            <div class="text-h6">{{ project.name }}</div>
            <div class="text-subtitle2">{{ project.info }}</div>
          </q-card-section>

          <q-card-actions>
            <q-btn
              flat
              color="primary"
              label="Link"
              :href="project.link"
              target="_blank"
              :disable="!project.link"
            />
            <q-btn flat color="secondary" label="Github" :href="project.github" target="_blank" />

            <q-space />

            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="project.expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="toggle(project)"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="project.expanded">
              <q-separator />
              <q-card-section class="text-subtitle2">
                <div>
                  Tech: <span class="">{{ project.tech }}</span>
                </div>
                <div>Learnt: {{ project.learnt }}</div>
              </q-card-section>
            </div>
          </q-slide-transition>
        </q-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: 'Curated',
          info: 'Favorite Project. Readwise equivalent for Pinterest, Notion',
          tech: 'Laravel, Vue, Cron jobs',
          learnt: 'Clean modular models, relations, seeders, scheduling',
          github: 'https://github.com/IshaHarmalkar/Digital_Garden',
          img: '/projects/curated/newsletter.png',
          link: '',
          exapanded: false,
        },
        {
          name: 'Pokedex',
          info: 'Explore pokemon stats, compare, genrate random pokemons',
          tech: 'laravel, Vue, Pokeapi',
          learnt: 'Laravel, Vue, external api integrations, wait times',
          github: 'https://github.com/IshaHarmalkar/Pokedex',
          img: '/projects/pokedex/Home.png',
          link: 'https://pokedex-app.ishaharmalkar.com/#/',
          exapanded: false,
        },
        {
          name: 'Realtime Weather',
          info: 'What is the weather today, indeed?',
          tech: 'Bootstrap, html, css, js, React',
          learnt: 'Basic Web Development',
          github: 'https://github.com/IshaHarmalkar/weather-react',
          img: '/projects/weather/weather_js.png',
          link: 'https://weatherproject2024.netlify.app/',
          exapanded: false,
        },
        {
          name: 'SARIMA Time Series Forecasting',
          info: 'Predict demand for NCY taxi.',
          tech: 'Python, Flask, React, Leaflet',
          learnt: 'Data cleaning, feature selections, training, flask apis',
          github: 'https://github.com/IshaHarmalkar/Predict_final',
          img: '/projects/sarima/sarima.jpg',
          link: '',
          exapanded: false,
        },
      ],
    }
  },

  methods: {
    toggle(project) {
      project.expanded = !project.expanded
    },
  },
}
</script>

<style lang="scss" scoped></style>
