<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="gradient-header">
      <q-toolbar>
        <q-toolbar-title>
          Rafek
        </q-toolbar-title>

        <q-btn flat dense label="About Us" @click="showAboutDialog = true" />

        <q-btn-toggle
          v-model="language"
          flat
          toggle-color="green-3"
          :options="[
            {label: 'EN', value: 'en'},
            {label: 'AR', value: 'ar'}
          ]"
        />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer elevated class="text-black text-center">
      <q-toolbar>
        <q-toolbar-title class="text-subtitle2">
          © {{ new Date().getFullYear() }} Rafek. All rights reserved.
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

    <q-dialog v-model="showAboutDialog">
      <q-card>
        <q-card-section>
          <div class="text-h6">About Us</div>
        </q-card-section>

        <q-card-section>
          Rafek is an innovative platform that helps organizations and businesses track their carbon footprint. We provide a comprehensive dashboard to visualize emissions data and use cutting-edge AI to predict future trends and recommend sustainable strategies.
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="Close" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

defineOptions({
  name: 'MainLayout'
})

const language = ref('en')
const showAboutDialog = ref(false)
</script>

<style lang="scss">
.q-header {
  .q-toolbar {
    .q-toolbar-title {
      font-size: 1.5rem;
      font-weight: bold;
    }
  }
}

.q-footer {
  background: linear-gradient(135deg, #a7dda8, #81b5df);
  .q-toolbar {
    min-height: 40px;
    .q-toolbar-title {
      font-size: 0.8rem;
      text-align: center;
    }
  }
}

.gradient-header {
  background: linear-gradient(135deg, #4CAF50, #2196F3);
}
</style>
