<template>
  <q-page class="q-mt-md">

    <div class="row flex flex-center">
      <div class="col-12 flex flex-center">
        <img alt="Logo" src="~assets/logo.svg" style="width: 200px; height: 200px" />

      </div>

      <div class="q-pa-md col-12">
        <q-carousel color="white" arrows infinite thumbnails height="50vh" v-model="slide">
          <q-carousel-slide :name="1" img-src="~assets/h1.jpg" style="height: 100%!important" />
          <q-carousel-slide :name="2" img-src="~assets/h2.jpg" />
          <q-carousel-slide :name="3" img-src="~assets/h3.jpg" />
          <q-carousel-slide :name="4" img-src="~assets/h4.jpg" />
        </q-carousel>
      </div>

      <div class="col-12 flex flex-center q-mt-xl">
        <q-btn round color="black" icon="chevron_left" @click="$router.push('/primary')" />
      </div>
    </div>

  </q-page>
</template>
<script setup>
import { ref } from 'vue'

const slide = ref(1)
</script>
