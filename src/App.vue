<template>
<v-app>
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-start  justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>Boardgames Stock</v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
      <router-view/>
    </v-content>
</v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data () {
    return {
      //
    }
  }
}
</script>
