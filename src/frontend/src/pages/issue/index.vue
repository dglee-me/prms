<template>
  <v-navigation-drawer permanent width="380">
    <v-list lines="three" class="data-wrapper overflow-y-auto">
      <v-list-item
        v-for="item in items"
        :key="item.id"
        :title="item.title"
        :subtitle="item.content"
        :ripple="false"
        border="s-sm t-sm e-sm"
        on-click="() => {}"
      >
        <template #prepend>
          <v-avatar color="blue" text="동근"/>
        </template>
      </v-list-item>
    </v-list>
    <div class="border-t-sm">
      <v-pagination active-color="primary" :length="4"></v-pagination>
    </div>
  </v-navigation-drawer>
</template>

<script setup>
const items = [
  {
    id: 1,
    title: "이슈 넘버1",
    content: "이슈 내용1",
  },
  {
    id: 2,
    title: "이슈 넘버2",
    content: "이슈 내용2",
  },
  {
    id: 3,
    title: "이슈 넘버3",
    content: "이슈 내용3",
  },
  {
    id: 4,
    title: "이슈 넘버4",
    content: "이슈 내용4",
  },
  {
    id: 5,
    title: "이슈 넘버5",
    content: "이슈 내용5",
  },
  {
    id: 6,
    title: "이슈 넘버6",
    content: "이슈 내용6",
  },
  {
    id: 7,
    title: "이슈 넘버7",
    content: "이슈 내용7",
  },
  {
    id: 8,
    title: "이슈 넘버8",
    content: "이슈 내용8",
  },
  {
    id: 9,
    title: "이슈 넘버9",
    content: "이슈 내용9",
  },
  {
    id: 10,
    title: "이슈 넘버10",
    content: "이슈 내용10",
  },
]
</script>

<style lang="scss" scoped>
.data-wrapper {
  height: calc(100% - 57px);
}
</style>
