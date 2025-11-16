<script setup>
import { onMounted } from 'vue'
import * as Cesium from 'cesium'
import 'cesium/Build/Cesium/Widgets/widgets.css'

onMounted(() => {
  const viewer = new Cesium.Viewer('cesiumContainer', {
    timeline: false,
    animation: false,
  })

  // để sau này debug từ console
  window.cesiumViewer = viewer
})
</script>

<template>
  <div id="cesiumContainer"></div>
</template>

<style>
html,
body,
#app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}

#cesiumContainer {
  width: 100vw;
  height: 100vh;
  display: block;
}
</style>
