<template>
  <q-page class="constrain q-pa-md">

    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8 q-col-gutter">
        <q-card
          v-for="post in posts"
          :key="post.id"
          class="card-post q-mb-md"
          bordered
          flat
        >
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img src="https://s.gravatar.com/avatar/ce7f3697e231df38b3ca6065848520da?s=80">
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label
              class="text-bold">danny__connell</q-item-label>
              <q-item-label caption>
                {{ post.location }}
              </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-img
            :src="post.imageURL"
          />
          <q-card-section>
            <div>{{ post.location }}</div>
            <div class="text-caption text-grey">{{ post.date | niceDate }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar size="48px">
              <img src="https://s.gravatar.com/avatar/ce7f3697e231df38b3ca6065848520da?s=80">
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label
            class="text-bold">danny__connell</q-item-label>
            <q-item-label caption>
              Daddy Connell
            </q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>
  </q-page>
</template>

<script>
import { date } from 'quasar'

export default {
  name: 'PageHome',
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: 'Golden Gate Bridge',
          date: 1731490299189,
          location: 'San Francisco, United States',
          imageURL: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 2,
          caption: 'Golden Gate Bridge',
          date: 1731490299189,
          location: 'Soon Pipisco, United States',
          imageURL: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 3,
          caption: 'Golden Gate Bridge',
          date: 1731490299189,
          location: 'Non Capisco, United States',
          imageURL: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
      ]
    }
  },
  filters: {
    niceDate(value) {
      return date.formatDate(value, 'MMMM D h:mmA')
    }
  }
}
</script>

<style lang="scss">
.card-post {
  .q-img {
    min-height: 200px;
  }
}
</style>
