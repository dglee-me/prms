<template>
  <v-app>
    <BaseAppBar />
    <BaseSideBar/>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script setup>
import BaseAppBar from "@/components/BaseAppBar.vue";
import BaseSideBar from "@/components/BaseSideBar.vue";
</script>
