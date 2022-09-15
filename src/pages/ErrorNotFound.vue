<template>
  <div class="fullscreen bg-black text-white text-center q-pa-md flex flex-center">
    <div>
      <div style="font-size: 30vh">
        404
      </div>

      <div class="text-h2" style="opacity:.69">
        The dev is doing shit.
      </div>

      <q-btn class="q-mt-xl" color="red-14" text-color="warning" unelevated to="/"
        label="A button that does literally nothing ffs" no-caps @click="$router.push('/primary')" />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ErrorNotFound'
})
</script>
