<template>
   <v-container>
    <v-card
    class="mx-auto"
    max-width="400"
  >


    <v-list lines="three" select-strategy="classic">
      

      <v-list-item value="notifications">
        <template v-slot:prepend="{ isActive }">

          <v-list-item-action start>
            <v-checkbox-btn :model-value="isActive"></v-checkbox-btn>
          </v-list-item-action>
        </template>

        <v-list-item-title>Notifications</v-list-item-title>

        <v-list-item-subtitle>
          Notify me about updates to apps or games that I downloaded
        </v-list-item-subtitle>
      </v-list-item>

      <v-list-item value="sound">
        <template v-slot:prepend="{ isActive }">
          <v-list-item-action start>
            <v-checkbox-btn :model-value="isActive"></v-checkbox-btn>
          </v-list-item-action>
        </template>

        <v-list-item-title>Sound</v-list-item-title>

        <v-list-item-subtitle>
          Auto-update apps at any time. Data charges may apply
        </v-list-item-subtitle>
      </v-list-item>

      <v-list-item value="widgets">
        <template v-slot:prepend="{ isActive }">
          <v-list-item-action start>
            <v-checkbox-btn :model-value="isActive"></v-checkbox-btn>
          </v-list-item-action>
        </template>

        <v-list-item-title>Auto-add widgets</v-list-item-title>

        <v-list-item-subtitle>
          Automatically add home screen widgets when downloads complete
        </v-list-item-subtitle>
      </v-list-item>
    </v-list>
  </v-card>
   </v-container>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>