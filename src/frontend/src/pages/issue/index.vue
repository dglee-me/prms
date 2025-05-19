<template>
  <div class="split-view">
    <!-- Left Panel -->
    <div class="left-panel">
      <div class="list-wrapper">
        <v-list lines="three">
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            :ripple="false"
            @click="">
            <template #prepend>
              <v-avatar color="blue" text="동근"></v-avatar>
            </template>
            <v-list-item-title>{{ item.author }}</v-list-item-title>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
            <v-list-item-subtitle>{{ item.content }}</v-list-item-subtitle>
          </v-list-item>
        </v-list>
      </div>
      <div class="pagination-wrapper">
        <v-pagination active-color="primary" :length="4"></v-pagination>
      </div>
    </div>
    <!-- Right Panel -->
    <div class="right-panel">
      <v-card v-if="selectedPost">
        <v-card-title>테스트1</v-card-title>
        <v-card-text>테스트용 더미 데이터</v-card-text>
      </v-card>
      <div v-else class="d-flex justify-center align-center" style="height: 100%;">
        선택된 게시글이 없습니다.
      </div>
    </div>
  </div>
</template>

<script setup>
const items = [
  {
    id: 1,
    author: "일동근",
    title: "[CSAP] CCE 취약점 조치",
    content: "- CM DB Master/Slave 최신화 필요 - 게시판 API 서버 커널 업데이트 필요",
  },
  {
    id: 2,
    author: "이동근",
    title: "이슈 넘버2",
    content: "이슈 내용2",
  },
  {
    id: 3,
    author: "삼동근",
    title: "이슈 넘버3",
    content: "이슈 내용3",
  },
  {
    id: 4,
    author: "사동근",
    title: "이슈 넘버4",
    content: "이슈 내용4",
  },
  {
    id: 5,
    author: "오동근",
    title: "이슈 넘버5",
    content: "이슈 내용5",
  },
  {
    id: 6,
    author: "육동근",
    title: "이슈 넘버6",
    content: "이슈 내용6",
  },
  {
    id: 7,
    author: "칠동근",
    title: "이슈 넘버7",
    content: "이슈 내용7",
  },
  {
    id: 8,
    author: "팔동근",
    title: "이슈 넘버8",
    content: "이슈 내용8",
  },
  {
    id: 9,
    author: "구동근",
    title: "이슈 넘버9",
    content: "이슈 내용9",
  },
  {
    id: 10,
    author: "십동근",
    title: "이슈 넘버10",
    content: "이슈 내용10",
  },
]
</script>

<style lang="scss" scoped>
.split-view {
  display: flex;
  height: calc(100vh - 64px); /* App Bar 높이만큼 빼줌 */
  overflow-y: hidden;
}

.left-panel {
  width: 30%;
  display: flex;
  flex-direction: column;
}

.list-wrapper {
  overflow-y: auto;
}

.pagination-wrapper {
  height: 57px;
}

.right-panel {
  width: 100%;
  overflow-y: auto;
}

.list-wrapper .v-list {
  padding: 0;
}
</style>
