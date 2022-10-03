<template>
  <q-page class="constrain q-pa-md">
    <q-card
    v-for="post in posts" :keys="posts.id"
     flat
     bordered
     class="card-post">
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">Dannu22</q-item-label>
          <q-item-label caption>
            San Franciso, United States
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />
      <img src="https://cdn.quasar.dev/img/parallax2.jpg">

      <q-card-section>
        <div>Golden gate </div>
        <div class="text-caption text-grey">June 10 9:04am</div>
      </q-card-section>

    </q-card>
  </q-page>
</template>

<script>


export default({
  name: 'PageHome',
  data(){
    return{
      posts:[
        {
          id: 1,
          cation:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg'

        },
        {
          id: 2,
          cation:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg'

        },
        {
          id: 3,
          cation:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg'

        },
        ,
        {
          id: 4,
          cation:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg'

        },

      ]
    }
  }
})
</script>
<style lang="sass">
.card-post
  .q-img
    min-height: 200px
</style>
