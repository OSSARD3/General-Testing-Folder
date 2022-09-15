<template>
  <q-layout view="hHh lpR fFf">
    <q-drawer v-model="left" side="left" width="300">
      <div v-for="index in 10" :key="index">
        test
      </div>
    </q-drawer>
    <q-page-container>
      <q-page class="background">
        <div class="q-pa-lg">
          <q-btn unelevated flat color="blue-10" text-color="blue-grey-11" @click="startComputing(2)"
            icon="cloud_upload" style="width: 100px;" class="absolute-top-right" />
        </div>
      </q-page>

    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const left = ref(true)
</script>
