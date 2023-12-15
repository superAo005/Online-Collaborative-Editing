<!-- eslint-disable prettier/prettier -->
<script setup>
import * as Y from "yjs"
import { QuillBinding } from "y-quill"
import Quill from "quill"
import QuillCursors from "quill-cursors"
import { WebsocketProvider } from "y-websocket"
import "quill/dist/quill.snow.css" // 使用了 snow 主题色
import { onMounted } from "vue"
//使用cursors插件
Quill.register("modules/cursors", QuillCursors)
onMounted(() => {
  const quill = new Quill(document.querySelector("#yjs"), {
    modules: {
      cursors: true,
      toolbar: [[{ header: [1, 2, false] }], ["bold", "italic", "underline"], ["image", "code-block"]],
      history: {
        userOnly: true
      }
    },
    placeholder: "",
    theme: "snow"
  })
  const ydoc = new Y.Doc() //y文档对象，保存需要共享的数据
  const ytext = ydoc.getText("quill") //创建名为quill的Text对象
  //连接到websocket服务端
  const provider = new WebsocketProvider("ws://localhost:1234", "quill-demo-room", ydoc)
  //数据模型绑定，再绑上光标对象
  const binding = new QuillBinding(ytext, quill, provider.awareness)
})
</script>

<template>
  <div id="yjs"></div>
</template>

<style scoped></style>
