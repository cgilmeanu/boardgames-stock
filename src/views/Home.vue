<template>
  <v-container fluid grid-list-lg>
    <v-layout row wrap>
      <template v-for="(item) in boardgames">
        <v-flex xs12 v-bind:key="item.id">
          <v-card color="lime lighten-4">
            <v-layout>
              <v-flex xs5>
                <div style="width: 300px; height: 300px">
                  <v-img v-bind:src="item.imageLink" aspect-ratio="1" height="300px" contain></v-img>
                </div>
              </v-flex>
              <v-flex xs7>
                <v-card-title primary-title>
                  <div>
                    <div class="headline">{{ item.title }}</div>
                    <div>{{ item.description }}</div>
                  </div>
                </v-card-title>
              </v-flex>
            </v-layout>
            <v-divider color="accent"></v-divider>
          </v-card>
        </v-flex>
      </template>
    </v-layout>
  </v-container>
</template>

<script lang="ts">
import Vue from 'vue'
import Axios from 'axios'

export default Vue.extend({
  name: 'home',
  data: () => {
    return {
      boardgames: []
    }
  },
  methods: {},
  created() {
    this.axios.get('http://localhost:3000/boardgames').then(result => (this.boardgames = result.data))
  }
})
</script>
