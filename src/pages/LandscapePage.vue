<template>
  <q-layout view="hHh lpR fFf">
    <q-drawer v-model="left" side="left" width="300">
      <div>
        <div class="row q-pa-md">
          <div class="col-10"></div>
          <div class="col-2">
            <q-btn round color="primary" text-color="white" icon="close" size="12px" @click="left = !left" />
          </div>
        </div>
        <q-separator />
        <div class="row flex flex-center">
          <div class="q-pa-md text=bold text-h5">Existing lesson content</div>
        </div>
        <q-separator />
        <div class="row flex flex-center text=bold text-h5">
          <div class="q-pa-md text=bold text-h5">Add new lesson content</div>
        </div>
        <div class="row">
          <q-list class="full-width">
            <q-item clickable v-for="(item, index) in menuItems" :key="index">
              <q-item-section avatar>
                <q-icon color="primary" :name="item.icon" />
              </q-item-section>
              <q-item-section class="text-body1">{{item.title}}</q-item-section>
            </q-item>
          </q-list>
        </div>
        <!--<div v-for="index in 10" :key="index" class="row">test</div>-->
      </div>
    </q-drawer>

    <q-page-container>
      <q-page class="background">
        <div class="q-pa-lg absolute-top-right">
          <q-btn unelevated color="secondary" text-color="blue-grey-11" @click="startComputing(2)" label="Publish"
            icon="cloud_upload" style="width: 150px" no-caps />
        </div>
        <div class="q-pa-md absolute-top-left" v-if="!left">
          <q-btn color="primary" round icon="menu" @click="left= !left" />
        </div>
        <div class="absolute-bottom flex flex-center q-pb-md">
          <div class="flex flex-center"
            style="width:400px;height:64px; background-color: rgba(94, 94, 94, 0.43); border-radius: 10px;">
            <div class="col-2 q-pa-sm">
              <q-btn round color="primary" icon="image" @click="onClick" />
            </div>
            <div class="col-2 q-pa-sm">
              <q-btn round color="primary" icon="book" @click="onClick" />
            </div>
            <div class="col-2 q-pa-sm">
              <q-btn round color="primary" icon="edit" @click="onClick" />
            </div>
            <div class="col-2 q-pa-sm">
              <q-btn round color="primary" icon="info" @click="onClick" />
            </div>
            <div class="col-2 q-pa-sm">
              <q-btn round color="primary" icon="door_back" @click="onClick" />
            </div>
          </div>
        </div>
        <div class="absolute-right flex flex-center containssvg">
          <div style="position:relative; height: 200px; width: 200px; border-radius: 50%; background-color: #F78D29;">

            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
              <path d="M5.88 4.12L13.76 12l-7.88 7.88L8 22l10-10L8 2z" fill="white" />
            </svg>

          </div>
        </div>
      </q-page>
    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const left = ref(true)

const menuItems = ref(
  [
    {
      index: 0,
      title: 'Add a PowerPoint',
      icon: 'picture_as_pdf'

    },
    {
      index: 1,
      title: 'Add a PDF',
      icon: 'picture_as_pdf'
    },
    {
      index: 2,
      title: 'Add a YouTube video or Google Slides',
      icon: 'link'
    },
    {
      index: 3,
      title: 'Add text',
      icon: 'text_increase'
    },
    {
      index: 4,
      title: 'Add a quiz',
      icon: 'quiz'
    }

  ]
)
</script>
