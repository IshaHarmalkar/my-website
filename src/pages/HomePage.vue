<template>
  <q-page>
    <div class="main-container">
      <div class="row">
        <div class="col-6">
          <div class="flex flex-center test-border q-mt-lg">
            <h3 class="text-start q-ma-none q-pa-none">
              Hi! I'm Isha — I build cool stuff for the web
            </h3>
            <h4 class="text-strart">
              From hackathons to real-world apps, I love turning ideas into full-stack magic with
              Laravel, Vue, and Node.js. Whether it’s crafting clean APIs, snappy UIs, or squeezing
              out extra performance, I’m all about creating things that work and feel good to use.
            </h4>
          </div>
          <div class="text-start">
            Check out what <a>bboks I'm reading</a>, finnd me on <a>Twitter</a>, or on
            <a>Linkedin</a>, or just <a>send me an email</a> saying hi.
          </div>
        </div>
        <div class="col-6">
          <div class="flex">
            <q-img :src="lineArtImage" fit="contain" />
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import lineArtImage from 'src/assets/home-media/line-art-transparent.png'
</script>

<style lang="scss" scoped>
.main-container {
  margin: 0 20px;
}
.test-border {
  border: 1px solid pink;
}
</style>
