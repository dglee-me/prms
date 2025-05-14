<template>
  <v-app-bar :elevation="0">
    <template #prepend>
      <v-app-bar-nav-icon />
    </template>
    <v-toolbar-title
      v-if="!isMobile"
      @click="$router.push('/')"
    >Crinity PRMS
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <template #append>
      <v-avatar color="blue" text="동근"/>
    </template>
  </v-app-bar>
</template>

<script setup>
import {useDisplay} from "vuetify/framework";

const isMobile = useDisplay().xs;
</script>

<style lang="scss">
.v-toolbar-title {
  max-width: 180px;
  cursor: pointer;
}
</style>
