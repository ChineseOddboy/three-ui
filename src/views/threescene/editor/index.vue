<template>
  <div>
    <a-button @click="creat" type="primary">Primary Button</a-button>
    <canvas class="canvas" id="renderCanvas"></canvas>
  </div>
</template>
<script lang="ts" setup>
import { defineComponent, onMounted, ref, reactive } from 'vue';
import { Playground } from './Playground';
import * as BABYLON from 'babylonjs';
let PG: any;
onMounted(() => {
  createScene();
});
function createScene() {
  const canvas = document.getElementById('renderCanvas') as HTMLCanvasElement;
  if (canvas) {
    PG = new Playground(canvas);
    PG.run();
  }
}
function creat(){
    console.log("1111");
    PG.addSohere("qwe",{ diameter: 2, segments: 32 },PG.scene);
}
</script>
<style scoped>
.canvas {
  width: 100%;
  height: 100%;
  touch-action: none;
}
</style>