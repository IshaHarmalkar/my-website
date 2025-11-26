<template>
  <q-layout view="hHh lpR fFf">
    <!-- Minimalistic Header -->
    <q-header class="bg-color text-black" height-hint="64">
      <q-toolbar class="q-py-sm">
        <q-toolbar-title class="text-h6 text-weight-light">
          <div class="flex items-center q-gutter-sm">
            <span class="cursive">Isha</span>
          </div>
        </q-toolbar-title>

        <div class="row items-center q-gutter-sm">
          <q-btn
            v-for="(link, index) in Links"
            :key="index"
            :label="link.name"
            :icon="link.icon"
            flat
            rounded
            dense
            color=""
            :dark-percentage="link.path"
            class="q-ma-xs"
          />
        </div>
      </q-toolbar>
    </q-header>

    <!-- Main Content Area -->
    <q-page-container class="q-pa-xl bg-color">
      <router-view />
    </q-page-container>

    <!-- Minimal Footer -->
    <q-footer class="bg-color text-grey-8 border">
      <q-toolbar class="q-py-xs" style="min-height: 40px">
        <q-space />
        <div class="text-caption">© 2025 Isha Harmalkar. All rights reserved.</div>
        <q-space />
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
export default {
  name: 'CustomLayout',

  data() {
    return {
      Links: [
        { name: 'Home', path: '/', icon: '' },
        { name: 'Internships', path: '/#internships', icon: '' },
        { name: 'Projects', path: '/#projects', icon: '' },
        { name: 'Websites', path: '/#frontend', icon: 'sloth' },
      ],
    }
  },
}
</script>

<style scoped>
/* Custom minimal styling */

/* Smooth transitions */
.q-tab {
  transition: all 0.2s ease;
}

.q-tab:hover {
  background-color: rgba(0, 0, 0, 0.04);
}

.bg-color-grd {
  background: radial-gradient(
    592px at 48.2% 50%,
    rgba(255, 255, 249, 0.6) 0%,
    rgb(160, 199, 254) 74.6%
  );
}
</style>
