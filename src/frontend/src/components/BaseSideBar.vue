<template>
  <v-navigation-drawer>
    <v-list nav>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        :to="item.path"
        :active="route.path === item.path"
        color="primary"
      >
        <template #prepend>
          <v-icon :icon="item.icon"></v-icon>
        </template>
        <v-list-item-title v-text="item.title"/>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup>
import {useRoute} from "vue-router";

const route = useRoute();

const items = [
  {
    title: "고객 관리",
    path: "/project",
    icon: 'mdi-account-group'
  },
  {
    title: "이슈 관리",
    path: "/issue",
    icon: 'mdi-bug'
  },
  {
    title: "업무 관리",
    path: "/task",
    icon: 'mdi-briefcase'
  }
];
</script>

<style lang="scss">
</style>
