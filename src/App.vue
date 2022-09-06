<template>
  <div class="main">
    <div class="container" id="container"></div>
  </div>
</template>

<script setup lang="ts">
// @ts-ignore
// import DiagramViewer from "@ggwork/diagramviewer";
import { onMounted } from "vue";

onMounted(() => {
  let data_url = "http://localhost:1337/api/diagrams/58";
  let container = document.querySelector("#container");
  // @ts-ignore
  new window.DiagramViewer(container, data_url);
});
</script>
<style>
.main {
  width: 100vw;
  height: 100vh;
}
.container {
  width: 500px;
  height: 300px;
  border: 1px solid #eee;
  margin: auto;
}
</style>
