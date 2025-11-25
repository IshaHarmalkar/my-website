<template>
  <div class="container">
    <div class="text-h3 text-primary">🌻Frontend Projects</div>
    <div class="row q-col-gutter-lg q-mt-md">
      <div v-for="(project, index) in projects" :key="index" class="col-12 col-sm-6 col-md-4">
        <q-card class="my-card" square>
          <img :src="project.img" fit="cover" style="height: 300px" />

          <q-card-section>
            <div class="text-h6">{{ project.name }}</div>
            <div class="text-subtitle2">{{ project.info }}</div>
          </q-card-section>

          <q-card-actions>
            <q-btn flat color="primary" label="Link" :href="project.link" target="_blank" />
            <q-btn flat color="secondary" label="Github" />

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
                <div>{{ project.tech }}</div>
                <div>{{ project.learnt }}</div>
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
          name: 'DreamHouse Challenge',
          info: 'Favorite Project. Readwise equivalent for Pinterest, Notion',
          tech: 'Laravel, Vue, Cron jobs',
          learnt: 'Clean modular models, relations, seeders, scheduling',
          github: 'https://github.com/IshaHarmalkar/Digital_Garden',
          img: '/frontend-work/house.png',
          link: 'https://dream-house-challenge.netlify.app/',
          exapanded: false,
        },
        {
          name: 'Curated Landing Page',
          info: 'Explore pokemon stats, compare, genreate random pokemons',
          tech: 'laravel, Vue, Pokeapi',
          learnt: 'Laravel, Vue, external api integrations, wait times',
          github: 'https://github.com/IshaHarmalkar/Pokedex',
          img: '/frontend-work/curated.png',
          link: 'https://curated-demo.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'Meme Treasure Box',
          info: 'What is the weather today, indeed?',
          tech: 'Bootstrap, html, css, js, React',
          learnt: 'Basic Web Development',
          github: 'https://github.com/IshaHarmalkar/weather-react',
          img: '/frontend-work/meme_box.png',
          link: 'https://meme-treausure-box-demo.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'Bright Design',
          info: 'Predict demand for NCY taxi.',
          tech: 'Python, Flask, React, Leaflet',
          learnt: 'Data cleaning, feature selections, training, flask apis',
          github: 'https://github.com/IshaHarmalkar/Predict_final',
          img: '/frontend-work/bright_blog.png',
          link: 'https://quasar-blog.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'First Portfolio Page',
          info: 'Predict demand for NCY taxi.',
          tech: 'Python, Flask, React, Leaflet',
          learnt: 'Data cleaning, feature selections, training, flask apis',
          github: 'https://github.com/IshaHarmalkar/Predict_final',
          img: '/frontend-work/first_portfolio.png',
          link: 'https://amz-portfolio.netlify.app/',
          exapanded: false,
        },
        {
          name: 'React Weather App',
          info: 'Weather Projects are a genre',
          tech: 'React, componets, component libraries',
          learnt: 'Component separation, noob level animations',
          github: 'https://github.com/IshaHarmalkar/Predict_final',
          img: '/projects/weather/weather_react.png',
          link: 'https://homework-week-5.netlify.app/',
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
