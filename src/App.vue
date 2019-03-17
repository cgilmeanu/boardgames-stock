<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <v-layout align-start justify-center>
          <v-flex xs12 sm12 md8>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>Boardgames Stock</v-toolbar-title>
                <v-spacer></v-spacer>
                <v-tabs class="tabs" right dark color="primary" slider-color="accent">
                  <v-tab grow="false" :to="{ name: 'home'}">Home</v-tab>
                  <v-tab grow="false" :to="{ name: 'about'}">About</v-tab>
                </v-tabs>
              </v-toolbar>
            </v-card>
          </v-flex>
        </v-layout>
        <v-layout align-start justify-center>
          <v-flex xs12 sm12 md8>
            <router-view/>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
    <v-footer>
      <v-layout justify-center>Copyright (c), 2019</v-layout>
    </v-footer>
  </v-app>
</template>
<script>
export default {
  name: 'App',
}
</script>

<style lang="scss" scoped>
@import '@/styles/global.scss';

.tabs {
  max-width: 50%;
}
</style>

