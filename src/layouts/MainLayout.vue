<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
      class="bg-white text-grey-10"
      bordered
    >
      <q-toolbar class="constrain">
        <q-btn
          to="/camera"
          class="large-screen-only q-mr-sm"
          icon="eva-camera-outline"
          size="18px"
          flat
          round
          dense
        />
        <q-separator
        class="large-screen-only"
          vertical
          spaced
        />
        <q-toolbar-title class="grand-hotel-regular text-bold">
          Quasagram
        </q-toolbar-title>
        <q-btn
          to="/"
          class="large-screen-only"
          icon="eva-home-outline"
          size="18px"
          flat
          round
          dense
        />
      </q-toolbar>
    </q-header>

    <q-footer
      class="bg-white small-screen-only"
      bordered
    >
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab
          icon="eva-home-outline"
          to="/"
        />
        <q-route-tab
          icon="eva-camera-outline"
          to="/camera"
        />
      </q-tabs>
    </q-footer>

    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  name: 'MainLayout',
  data () {
    return {

    }
  }
}
</script>

<style lang="scss">
.q-toolbar {
  @media (min-width: $breakpoint-xs-max) {
    height: 77px;
  }
}
.q-toolbar__title {
  font-size: 30px;
  @media (max-width: $breakpoint-xs-max) {
    text-align: center;
  }
}
.q-footer {
  .q-tab__icon {
    font-size: 30px;
  }
}
</style>
