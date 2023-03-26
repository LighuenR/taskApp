<template>
  <v-app id="inspire">
      <v-navigation-drawer
      v-model="drawer"
      app
      theme="dark"
    >
      <v-list  nav>
        <v-container>
        <v-list-item-title>Vuetify Todo</v-list-item-title>
        <v-list-item-subtitle>Not ready</v-list-item-subtitle>
        </v-container>
   
        <v-list-item prepend-icon="mdi-view-dashboard" title="Todo" value="inbox"></v-list-item>
        <v-list-item prepend-icon="mdi-account-supervisor-circle" title="Supervisors" value="supervisors"></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Aplication</v-toolbar-title>
    </v-app-bar>

    <v-main>
     <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ drawer: null }),
  }
</script>