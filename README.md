# workflow-vue
Workflow drawing and configuration based on vue3

<p align="center">
  <a href="https://cn.vuejs.org/"><img src="https://img.shields.io/badge/%3C%2F%3E-Vue3-blue" alt="Vue3"></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/license-MIT-blue" alt="License"></a>
  <a href="README.md"><img src="https://img.shields.io/badge/%E6%96%87%E6%A1%A3-%E4%B8%AD%E6%96%87-blue" alt="Document"></a>
  <a href="https://www.npmjs.com/package/workflow-vue"><img src="https://img.shields.io/badge/npm-v14.0.0-blue" alt="Npm"></a>
</p>


## 用法
```vue
<template>
  <WorkflowVue ref="workflowRef"></WorkflowVue>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import WorkflowVue from 'workflow-vue'
import 'workflow-vue/dist/style.css'

import config from './config'

const workflowRef = ref()

onMounted(() => {
  workflowRef.value?.setConfig(config)
})
<script>
```

## 新的想法
鉴于原作者已经半年多没有维护
有一下的优化想法
 - 节点可以复制（Ctrl或者其他的方式），后续可以加入整块的复制
 - 四周边框拖动，可以拉伸节点，而不是拖拽
 - ～～实现中线的吸附～～（已实现）
 - 实现自动调整resize（可能会借鉴alibaba Butterfly）
