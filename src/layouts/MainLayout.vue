<template>
  <q-layout view="lHh Lpr lFf">
    <q-header unelevated>
      <q-toolbar class="bg-grey-10" align="center">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          CC
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-black"
    >
      <q-list>
        <q-item-label
          header
          class="text-white"
        >
          Menu
        </q-item-label>
        <q-item clickable active-class="active" class="text-white" exact v-ripple :to="{ name: 'dashboard'}">
          <q-item-section avatar>
            <q-icon name="av_timer"/>
          </q-item-section>

          <q-item-section>
            Dashboard
          </q-item-section>
        </q-item>
                <q-item clickable active-class="active" class="text-white" exact v-ripple :to="{ name: 'inputMateri'}">
          <q-item-section avatar>
            <q-icon name="input" />
          </q-item-section>

          <q-item-section>
            Input Materi
          </q-item-section>
                </q-item>
                <q-item clickable active-class="active" class="text-white" exact v-ripple :to="{ name: 'LihatKrs'}">
          <q-item-section avatar>
            <q-icon name="date_range" />
          </q-item-section>

          <q-item-section>
            Lihat KRS
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',

  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
