<template>
  <q-page class="row items-center justify-evenly">

    <q-card class="my-card">
      <q-card-section>
        <div class="text-h6 q-mb-xs">Our Changing Planet</div>
        <div class="row no-wrap items-center">
          <q-rating size="18px" v-model="stars" :max="5" color="warning" />
          <span class="text-caption text-grey q-ml-sm">4.2 (551)</span>
        </div>
      </q-card-section>

      <img src="https://cdn.quasar.dev/img/mountains.jpg">
    </q-card>
  </q-page>

</template>

<script lang="ts">




import { useQuasar } from 'quasar';
import {ref} from 'vue';
export default {
  name: 'IndexPage',

  setup() {
    const $q = useQuasar();
   $q.dark.set(true);


    return { stars: ref(4) };
  },
};
</script>
