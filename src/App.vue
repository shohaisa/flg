<template>
  <div class="common-layout">
    <el-container>
      <el-header class="header" ><h2>Мой профиль</h2></el-header>
      <el-main class="main"><router-view/></el-main>
      <el-footer class="footer">
        <FooterComponent />
      </el-footer>
    </el-container>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.common-layout {
  height: 100vh;
  display: flex;
  flex-direction: column;
}
.header {
  text-align: start;
}
main {
  flex: 1;
}
</style>
<script setup>
import FooterComponent from '@/components/FooterComponent.vue'
</script>
