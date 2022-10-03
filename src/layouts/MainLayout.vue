<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
    class="bg-white text-grey-10"
    bordered
    >
      <q-toolbar>
        <q-toolbar-title
        class="text-grand-hotel text-bold"

         >
          QuasarGram
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-footer
    class="bg-white"
    bordered>
          <q-tabs
          class="text-grey-10"
          active-color="primary"
          indicator-color="transparent"
      >
        <q-route-tab  icon="eva-home-outline"
         to="/"
         />
        <q-route-tab
         icon="eva-camera-outline"
        to="/camera" />
      </q-tabs>
      </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default ({
  name: 'MainLayout',
  components: {

  },

})
</script>
<style lang="sass">
.q-toolbar__title
    text-align: center
.q-footer
  .q-tab_icon
    font-size: 30px
</style>
