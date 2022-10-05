<template>
  <q-page class="constrain q-pa-md">
    <q-card v-for="(post,index) in posts"
    :key="posts.id"
    class="card-post q-mb-md"
     flat
     bordered
    >
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">Dannu22</q-item-label>
          <q-item-label caption>
           {{posts.location}}
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />
      <q-img :src="this.posts[index].img" />

      <q-card-section>
        <div>{{ posts.caption }}</div>
        <div class="text-caption text-grey">{{this.posts[index].date | niceDate}}</div>
      </q-card-section>

    </q-card>
  </q-page>
</template>

<script>

import { date } from 'quasar'

export default{
  name: 'PageHome',
  data(){
    return {
      posts: [
        {
          id: 1,
          caption:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          img:'https://www.makro.co.za/sys-master/images/h2a/h41/8904185970718/silo-MIN_157613_EAA_large?quality=340x372'

        },
        {
          id: 2,
          caption:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          img:'https://cdn.quasar.dev/img/parallax2.jpg'

        },
        {
          id: 3,
          caption:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          img:'https://cdn.quasar.dev/img/parallax2.jpg'

        },

        {
          id: 4,
          caption:'goldren gate bridge',
          date: 1591776655504,
          location:'San Franciso , United States',
          img:'https://cdn.quasar.dev/img/parallax2.jpg'

        },

      ]
    }
  },
  filters:{
    niceDate(value) {
      return date.formatDate(value, 'HH:ssA Do-MMM-YYYY' )
    }
  }
}
</script>
<style lang="sass">
.card-post
  .q-img
    min-height: 200px
</style>
