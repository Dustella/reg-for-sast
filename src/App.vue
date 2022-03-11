<template>
  <main-container>
  <h1>一个小时搓出来的签到系统</h1>
  你要是敢刷新页面 特菈学姐会把你打死
    <el-input
      placeholder="输入名字的拼音首字母"
      size="large"
      v-model="keyword"
    ></el-input>
    例如你叫余翰文就输入YHW
    <reg-card :keyword="keyword"></reg-card>
  </main-container>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import MainContainer from "./components/container.vue";
import RegCard from "./components/RegCard.vue";

const keyword = ref("");
</script>

<style lang="scss"></style>
