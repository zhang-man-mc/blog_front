<script>
import AppHeader from './AppHeader.vue'
export default {
  components: {
    AppHeader
  }
}
</script>

<template>
  <div class="common-layout">
    <el-container>
      <el-header>
        <AppHeader />
      </el-header>
      <el-main>
        <el-scrollbar>
          <router-view />
        </el-scrollbar>
      </el-main>
    </el-container>
  </div>
</template>

<style>
.el-header {
  height: 45px;
  background-color: #000000;
}
.el-scrollbar {
  /* 6vh header高度
    3vh 是随机添加的
  */
  height: calc(100vh - 6vh - var(--el-main-padding) * 2 - 3vh);
}
body {
  /* 移动端点击可点击元素时，出现蓝色默认背景色 */
  -webkit-tap-highlight-color: transparent;
}

</style>
