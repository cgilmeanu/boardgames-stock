<template>
  <v-content>
    <v-layout justify-center row>
      <v-flex class="headline" pt-4 text-xs-center>A simple and lightweight boardgames shelf</v-flex>
    </v-layout>
    <v-layout justify-center row>
      <v-flex class="title" pt-5 text-xs-center>List of technologies</v-flex>
    </v-layout>
    <v-container grid-list-sm fluid>
      <v-layout justify-center row wrap>
        <v-list two-line>
          <template v-for="(tech, index) in technologyStack">
            <v-divider v-bind:key="index" v-if="tech.divider"></v-divider>
            <v-list-tile v-else v-bind:key="tech.title" @click.prevent="navigateTo(tech.link)">
              <v-list-tile-content>
                <v-list-tile-title class="title">{{ tech.title }}</v-list-tile-title>
                <v-list-tile-sub-title class="subheading">{{ tech.subtitle }}</v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </template>
        </v-list>
      </v-layout>
    </v-container>
  </v-content>
</template>
<script lang="ts">
import Vue from 'vue'
import router from '@/router'

export default Vue.extend({
  data: () => {
    return {
      technologyStack: [
        {
          title: 'Vue',
          subtitle: 'A progressive framework for building user interfaces',
          link: 'https://vuejs.org/'
        },
        { divider: true },
        {
          title: 'Vuetify',
          subtitle: 'Material Design Component Framework',
          link: 'https://vuetifyjs.com'
        }
      ]
    }
  },
  methods: {
    navigateTo(link: string) {
      window.open(link, '_blank')
    }
  }
})
</script>

