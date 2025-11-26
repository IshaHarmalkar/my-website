<template>
  <q-page>
    <div class="main-container">
      <div class="row items-center">
        <div class="col">
          <div class="text-h3">Hi! I am Isha</div>
          <div>
            <div>
              Backend Software engineer from Goa, India.<br />
              I like to build cool stuff, work with cool people and learn cool things.
            </div>
            <div class="text-grey">
              p.s Cool is highly subjective. Mainly I just want to be good
            </div>

            <!-- <div class="text-h6">Laravel | VueJs | Python</div> -->

            <div class="text-h6">Always open to banter.</div>
            <div class="contact-container flex justify-between q-mt-sm">
              <q-btn
                outline
                color="red"
                href="https://drive.google.com/file/d/1KVJv7FNgll8MPulgVu2N6TGqShh_8Gxq/view?usp=sharing"
                target="_blank"
                label="Resume"
              />
              <q-btn
                outline
                color="red"
                href="https://www.linkedin.com/in/isha-harmalkar-0baa8a2b9/"
                label="Linkedin"
                target="_blank"
              />
              <q-btn
                outline
                color="red"
                href="https://x.com/IshaHarmalkar"
                label="Twitter"
                target="_blank"
              />
              <q-btn
                outline
                color="red"
                href="mailto:harmalkarisha@gmail.com"
                label="Mail"
                target="_blank"
              />
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
    <frontend-work class="space" />
  </q-page>
</template>

<script>
import ProjectWork from 'src/components/ProjectWork.vue'
import WorkExperience from 'src/components/WorkExperience.vue'
import FrontendWork from 'src/components/FrontendWork.vue'

export default {
  components: { WorkExperience, ProjectWork, FrontendWork },
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
