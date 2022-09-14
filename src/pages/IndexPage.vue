<template>
  <q-page class="q-mt-md">

    <div class="row flex flex-center">
      <div class="col-12 flex flex-center">
        <img alt="Logo" src="~assets/logo.svg" style="width: 200px; height: 200px" />

      </div>
      <div class="col-12 flex flex-center q-mt-md">
        <q-circular-progress indeterminate size="50px" :thickness="0.25" color="black" track-color="blue-grey-7" />
      </div>
      <div class="col-12 flex flex-center q-mt-xl">
        <q-btn round color="black" icon="expand_more" @click="$router.push('/secondary')" />
      </div>
    </div>

  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
