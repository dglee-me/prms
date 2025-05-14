<template>
  <v-navigation-drawer>
    <v-list nav>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        :to="item.path"
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
import {onMounted} from 'vue';
import {useRoute} from 'vue-router';

const route = useRoute();

onMounted(() => {
  console.log(route);
  console.log(route.params);  // 동적 라우트 매개변수
  console.log(route.query);   // URL의 쿼리 매개변수
  console.log(route.name);    // 라우트 이름
  console.log(route.path);    // 라우트 경로
  console.log(route.hash); // {url}?#sectionId
});

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
