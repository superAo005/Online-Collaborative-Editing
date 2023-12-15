<template>
  <el-tiptap v-model:content="content" :extensions="extensions" />
</template>

<script setup>
import { ref } from "vue"
import {
  // 需要的 extensions
  Doc,
  Text,
  Paragraph,
  Heading,
  Bold,
  Underline,
  Italic,
  Strike,
  BulletList,
  OrderedList,
  Table,
  Color,
  Highlight,
  Print,
  Fullscreen,
  SelectAll,
  FontFamily,
  FontSize
} from "element-tiptap"

// 编辑器的 extensions
// 它们将会按照你声明的顺序被添加到菜单栏和气泡菜单中
const extensions = [
  Doc,
  Text,
  Paragraph,
  Heading.configure({ level: 5 }),
  Bold.configure({ bubble: true }), // 在气泡菜单中渲染菜单按钮
  Underline.configure({ bubble: true, menubar: false }), // 在气泡菜单而不在菜单栏中渲染菜单按钮
  Italic,
  Strike,
  BulletList,
  OrderedList,
  Table,
  Color,
  Highlight,
  Print,
  Fullscreen,
  SelectAll,
  FontFamily,
  FontSize
]

// 编辑器的内容
const content = ref(`
  <h1>Heading</h1>
  <p>This Editor is awesome!</p>
`)
</script>
