<template>
  <el-card v-for="i of infos" v-show="showcard(i.k)" :key="i.name">
    {{ i.name }}
    <el-button @click="check(i.name)" :type="i.state ? 'default' : 'primary'">{{
      i.state ? "已签到" : "签到"
    }}</el-button>
  </el-card>
</template>

<script lang="ts" setup>
import { reactive } from "vue";

const props = defineProps({
  keyword: String,
});

const showcard = (sx: string): boolean => {
  if (props.keyword) {
    if (!sx.startsWith(props.keyword.toUpperCase())) {
      return false;
    }
  }
  return true;
};

// let infos = reactive([] as Array<{ name: string; state: boolean; k: string }>);

// let store = localStorage.getItem("infos");
// if (store && store != "") {
// //   infos = JSON.parse(store);
// //   console.log(infos);
// } else {
let infos = reactive([
  { name: "	王雨轩	", state: false, k: "WYX" },
  { name: "	王程平	", state: false, k: "WCP" },
  { name: "	王楠	", state: false, k: "WN" },
  { name: "	梁城铭	", state: false, k: "LCM" },
  { name: "	杨一帆	", state: false, k: "YYF" },
  { name: "	李昊阳	", state: false, k: "LHY" },
  { name: "	李东旭	", state: false, k: "LDX" },
  { name: "	王启璇	", state: false, k: "WQX" },
  { name: "	李茹兰	", state: false, k: "LRL" },
  { name: "	韩仲江	", state: false, k: "HZJ" },
  { name: "	田野	", state: false, k: "TY" },
  { name: "	周健	", state: false, k: "ZJ" },
  { name: "	胡平	", state: false, k: "HP" },
  { name: "	陈昶旭	", state: false, k: "CYX" },
  { name: "	李姗芳	", state: false, k: "LSF" },
  { name: "	郑振廷	", state: false, k: "ZZT" },
  { name: "	林芸颉	", state: false, k: "LYJ" },
  { name: "	葛鸣城	", state: false, k: "GMC" },
  { name: "	张一博	", state: false, k: "ZYB" },
  { name: "	张木梓	", state: false, k: "ZMX" },
  { name: "	倪俊锋	", state: false, k: "NJF" },
  { name: "	池锵云	", state: false, k: "CQY" },
  { name: "	谢炜炜	", state: false, k: "XWW" },
  { name: "	魏林东	", state: false, k: "WLD" },
  { name: "	杨韩森	", state: false, k: "YHS" },
  { name: "	焦冠杰	", state: false, k: "JGJ" },
  { name: "	邹恒彬	", state: false, k: "ZHB" },
  { name: "	莫光晖	", state: false, k: "MGH" },
  { name: "	汪义琅	", state: false, k: "WYL" },
  { name: "	赵思鉴	", state: false, k: "ZSJ" },
  { name: "	杨宇航	", state: false, k: "YYH" },
  { name: "	班克坤	", state: false, k: "BKK" },
  { name: "	刘城安	", state: false, k: "LCA" },
  { name: "	谭懿宸	", state: false, k: "TYC" },
  { name: "	丁韦奕	", state: false, k: "DWY" },
  { name: "	施钧文	", state: false, k: "SJW" },
  { name: "	谢鑫	", state: false, k: "XX" },
  { name: "	陈嵚杰	", state: false, k: "CQJ" },
  { name: "	周易潇	", state: false, k: "ZYX" },
  { name: "	林琪	", state: false, k: "LQ" },
  { name: "	曾嘉智	", state: false, k: "ZJZ" },
  { name: "	王锦川	", state: false, k: "WJC" },
  { name: "	黄正汉	", state: false, k: "HZH" },
  { name: "	李子怡	", state: false, k: "LZY" },
  { name: "	袁星	", state: false, k: "YX" },
  { name: "	张艺浓	", state: false, k: "ZYN" },
  { name: "	吕灿	", state: false, k: "LC" },
  { name: "	贾梦婷	", state: false, k: "JMT" },
  { name: "	杨征	", state: false, k: "YZ" },
  { name: "	杨雨萱	", state: false, k: "YYX" },
  { name: "	邱伟良	", state: false, k: "QWL" },
  { name: "	夏斯涛	", state: false, k: "XST" },
  { name: "	于航	", state: false, k: "YH" },
  { name: "	施非凡	", state: false, k: "SFF" },
  { name: "	李奕杨	", state: false, k: "LYY" },
  { name: "	樊凯	", state: false, k: "FK" },
  { name: "	李响	", state: false, k: "LX" },
  { name: "	董洪康	", state: false, k: "DYK" },
]);
// }

const check = (name: string) => {
  for (let i of infos) {
    if (i.name == name) {
      i.state = !i.state;
      console.log("a");
    }
  }
  //   localStorage.clear();
  //   localStorage.setItem("infos", JSON.stringify(infos));
};
</script>

<style>
.el-button {
  float: right;
}
</style>
