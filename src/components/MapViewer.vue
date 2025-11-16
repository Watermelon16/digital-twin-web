<script setup>
import { onMounted } from 'vue'
import * as Cesium from 'cesium'
import 'cesium/Build/Cesium/Widgets/widgets.css'

let viewer

onMounted(() => {
  viewer = new Cesium.Viewer('mapContainer', {
    animation: false,
    timeline: false,
    baseLayerPicker: true,
  })

  window.cesiumViewer = viewer
})
</script>

<template>
  <div id="mapContainer"></div>
</template>

<style scoped>
#mapContainer {
  width: 100%;
  height: 100%;
  display: block;
}
</style>
