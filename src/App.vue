<template>
  <v-app id="inspire">
    <app-header/>
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {


  components:{
    AppHeader
  },

  data: () => ({ drawer: null }),
}
</script>