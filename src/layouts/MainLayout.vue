<template>
  <q-layout view="hHh lpR fFf">
    <q-header reveal elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          <q-avatar>

          </q-avatar>
          Title
        </q-toolbar-title>

  <div class="q-pa-md">
    <div class="q-gutter-y-md" style="max-width: 400px">
      <q-tabs
        v-model="tab"
        class="bg-primary text-white shadow-2"
      >
        <q-tab name="mails" icon="mail" label="Mensajes">
          <q-badge color="red" floating>2</q-badge>
        </q-tab>
        <q-tab name="alarms" icon="alarm" label="Alertas">
          <q-badge color="red" floating>10+</q-badge>
        </q-tab>

      </q-tabs>
    </div>
  </div>


      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="Page One" />
        <q-route-tab to="/page2" label="Page Two" />
        <q-route-tab to="/page3" label="Page Three" />
      </q-tabs>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" overlay bordered>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
         
          <div align="center">copyright</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>
<script>
import { ref } from 'vue';

export default {
  setup() {
    const leftDrawerOpen = ref(false);
    const rightDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      tab: ref('mails'),
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },

      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
