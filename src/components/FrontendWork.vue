<template>
  <div class="container">
    <div class="text-h3 text-primary">🌻Frontend Projects</div>
    <div class="row q-col-gutter-lg q-mt-md">
      <div v-for="(project, index) in projects" :key="index" class="col-12 col-sm-6 col-md-4">
        <q-card class="my-card card-bg" square>
          <img :src="project.img" fit="cover" style="height: 300px" />

          <q-card-section>
            <div class="text-h6">{{ project.name }}</div>
            <div class="text-subtitle2">{{ project.info }}</div>
          </q-card-section>

          <q-card-actions>
            <q-btn flat color="primary" label="Link" :href="project.link" target="_blank" />
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
          info: 'Was madde for a SheCodes challenge, I like it a lot',
          tech: 'Bootstrap, html, css',
          learnt: 'Brushed up on my frontend skills.',
          github: 'https://github.com/IshaHarmalkar/sheCodes-challenge-house',
          img: '/frontend-work/house.png',
          link: 'https://dream-house-challenge.netlify.app/',
          exapanded: false,
        },
        {
          name: 'Curated Landing Page',
          info: 'Love it. Made it for Pinterest Api request. Got Approved!',
          tech: 'Quasar, Vuejs',
          learnt: 'Having a ready to code design is marvelous.',
          github: 'https://github.com/IshaHarmalkar/garden-frontend',
          img: '/frontend-work/curated.png',
          link: 'https://curated-demo.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'Meme Treasure Box',
          info: 'Another Pinterest Submission.',
          tech: 'Quasar, vue js',
          learnt: 'Fun web pages are fun to code. Enlightened.',
          github: 'https://github.com/IshaHarmalkar/meme-app-demo',
          img: '/frontend-work/meme_box.png',
          link: 'https://meme-treausure-box-demo.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'Bright Design',
          info: 'Built in order to learn quasar.',
          tech: 'Quasar, Vue.js',
          learnt: 'I remember I tried to replicate a ghost template that was super cool',
          github: 'https://github.com/IshaHarmalkar/Quasar-blog',
          img: '/frontend-work/bright_blog.png',
          link: 'https://quasar-blog.netlify.app/#/',
          exapanded: false,
        },
        {
          name: 'First Portfolio Page',
          info: 'Built during one of Shecodes workshop.',
          tech: 'Bootstrap, 12 grid rule, responsive design.',
          learnt: 'Responsive design',
          github: 'https://github.com/IshaHarmalkar/portfolio-1',
          img: '/frontend-work/first_portfolio.png',
          link: 'https://amz-portfolio.netlify.app/',
          exapanded: false,
        },
        {
          name: 'React Weather App',
          info: 'Maybe I am too much into weather🐼',
          tech: 'React, components, component libraries',
          learnt:
            'Component separation, baby level animations and a really cool react concept I cannot recall the name of',
          github: 'https://github.com/IshaHarmalkar/my-app',
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
