<template>
    <v-navigation-drawer v-model="drawer" app theme="dark">
      <v-list nav>
        <v-container>
          <v-list-item-title>Vuetify Todo</v-list-item-title>
          <v-list-item-subtitle>Not ready</v-list-item-subtitle>
        </v-container>

        <v-list-item to="/" prepend-icon="mdi-view-dashboard" title="Home" value="Indox"></v-list-item>
        <v-list-item to="/about" prepend-icon="mdi-account-supervisor-circle" title="About"
          value="supervisors"></v-list-item>
        <v-list-item to="/todo" prepend-icon="mdi-format-list-checks" title="Todo" value="supervisors"></v-list-item>

      </v-list>
    </v-navigation-drawer>


    <v-app-bar app color="teal-darken-4" image="https://picsum.photos/id/230/1920/1080">

      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-app-bar-title>Vuetify Todo</v-app-bar-title>

    </v-app-bar>

</template>
  
<script>
export default {
  data: () => ({ drawer: null }),
}
</script>