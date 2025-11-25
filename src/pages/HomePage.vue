<template>
  <q-page>
    <div class="main-container">
      <div class="row items-center">
        <div class="col">
          <div class="text-h3">Hi! I am Isha</div>
          <div>
            <p>
              Software engineer from India.<br />
              I like to build cool stuff, learn as build and lalllalaa
            </p>
            <!-- <div class="text-h6">Laravel | VueJs | Python</div> -->

            <div class="text-h6">Always opent to banter.</div>
            <div class="contact-container flex justify-between q-mt-sm">
              <q-btn outline color="red" label="Resume" />
              <q-btn outline color="red" label="Linkedin" />
              <q-btn outline color="red" label="Twitter" />
              <q-btn outline color="red" label="Mail" />
            </div>
          </div>
        </div>
        <div class="col">
          <q-img src="/home-media/line-art-transparent.png" />
        </div>
      </div>
    </div>

    <!-- Work Experience -->
    <work-experience class="space" />

    <!-- Project Work -->
    <project-work class="space" />
  </q-page>
</template>

<script>
import ProjectWork from 'src/components/ProjectWork.vue'
import WorkExperience from 'src/components/WorkExperience.vue'

export default {
  components: { WorkExperience, ProjectWork },
}
</script>

<style lang="scss" scoped>
.main-container {
  margin: 0 20px;
}
.test-border {
  border: 1px solid pink;
}

.space {
  margin: 160px 0;
}
</style>
