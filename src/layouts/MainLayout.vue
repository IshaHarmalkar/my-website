<template>
  <q-layout view="hHh lpR fFf">
    <!-- Minimalistic Header -->
    <q-header class="bg-white text-black" height-hint="64">
      <q-toolbar class="q-py-sm">
        <q-toolbar-title class="text-h6 text-weight-light">
          <div class="flex items-center q-gutter-sm">
            <span class="cursive">Isha Harmalkar</span>
          </div>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <!-- Main Content Area -->
    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>

    <!-- Minimal Footer -->
    <q-footer class="bg-white text-grey-6 shadow-up-1">
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
}
</script>

<style scoped>
/* Custom minimal styling */
.q-header {
  /* border-bottom: 1px solid #e0e0e0; */
}

.q-footer {
  border-top: 1px solid #e0e0e0;
}

/* Smooth transitions */
.q-tab {
  transition: all 0.2s ease;
}

.q-tab:hover {
  background-color: rgba(0, 0, 0, 0.04);
}
</style>
