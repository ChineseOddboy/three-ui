<template>
    <div>
        <canvas id="renderCanvas"></canvas>
    </div>
</template>
<script setup>
import { Playground } from "./Playground"

window.addEventListener('DOMContentLoaded', () => {
    const canvas = document.getElementById('renderCanvas') as HTMLCanvasElement;
    let playground = new Playground(canvas);
    playground.run();
});
</script>