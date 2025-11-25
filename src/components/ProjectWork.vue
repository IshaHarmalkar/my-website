<template>
  <div class="container">
    <div class="text-h3 text-primary">🌻My Projects</div>
    <div class="row q-col-gutter-lg q-mt-md">
      <div v-for="(project, index) in projects" :key="index" class="col-12 col-sm-6 col-md-4">
        <q-card class="my-card" square>
          <img :src="project.img" fit="cover" style="height: 300px" />

          <q-card-section>
            <div class="text-h6">{{ project.name }}</div>
            <div class="text-subtitle2">{{ project.info }}</div>
          </q-card-section>

          <q-card-section class="q-pt-none">
            {{ lorem }}
          </q-card-section>
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
        },
        {
          name: 'Pokedex',
          info: 'Explore pokemon stats, compare, genreate random pokemons',
          tech: 'laravel, Vue, Pokeapi',
          learnt: 'Laravel, Vue, external api integrations, wait times',
          github: 'https://github.com/IshaHarmalkar/Pokedex',
          img: '/projects/pokedex/Home.png',
        },
        {
          name: 'Realtime Weather',
          info: 'What is the weather today, indeed?',
          tech: 'Bootstrap, html, css, js, React',
          learnt: 'Basic Web Development',
          github: 'https://github.com/IshaHarmalkar/weather-react',
          img: '/projects/weather/weather_js.png',
        },
        {
          name: 'SARIMA-based Time Series Forecasting for NYC Taxi Demand',
          info: 'Predict demand for NCY taxi.',
          tech: 'Python, Flask, React, Leaflet',
          learnt: 'Data cleaning, feature selections, training, flask apis',
          github: 'https://github.com/IshaHarmalkar/Predict_final',
          img: '/projects/sarima/sarima.jpg',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
