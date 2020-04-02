<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-side-icon @click="toggleSideMenu"></v-toolbar-side-icon>
      <v-toolbar-title class="headline text-uppercase">
        <span>マイアドレス帳</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <SideNuv />
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>

import { mapActions } from 'vuex'
import SideNuv from './components/SideNuv'
export default {
  name: 'App',
  components: {
    SideNuv
  },
  data () {
    return {
      //
    }
  },
  methods: {
    openSideMenu () {
      this.$store.dispatch('toggleSideMenu')
    },
    ...mapActions(['toggleSideMenu'])
  }
}
</script>
