<script setup lang="ts">
defineProps<{ msg: string }>()
console.log("come in");
const openFile = async () => {
  const a = await window.chrome.webview.hostObjects.fileController.OpenFileDialog();
}
const saveFile = async () => {
  const a = await window.chrome.webview.hostObjects.fileController.SaveFileDialog();
}

</script>

<template>
  <h1>{{ msg }}</h1>
  <button @click="openFile">open file</button>
  <button @click="saveFile">save file</button>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
