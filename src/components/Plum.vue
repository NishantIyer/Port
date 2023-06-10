<template>
  <div class="canvas-container">
    <canvas ref="el" :width="size.width" :height="size.height" />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, reactive } from 'vue'
import { useWindowSize } from '@vueuse/core'

const el = ref<HTMLCanvasElement | null>(null)
const size = reactive(useWindowSize())

let animationFrameId: number | null = null

function drawBackground(ctx: CanvasRenderingContext2D): void {
  ctx.fillStyle = '#000000' // Set the background color to black
  ctx.fillRect(0, 0, size.width, size.height)
}

function animateBackground(ctx: CanvasRenderingContext2D): void {
  function update() {
    drawBackground(ctx)
    animationFrameId = requestAnimationFrame(update)
  }

  update()
}

onMounted(() => {
  const canvas = el.value!
  const ctx = canvas.getContext('2d')!
  canvas.width = size.width
  canvas.height = size.height

  animateBackground(ctx)
})

// Clean up animation frame on component unmount
const { onBeforeUnmount } = require('vue')
onBeforeUnmount(() => {
  if (animationFrameId) {
    cancelAnimationFrame(animationFrameId)
  }
})
</script>

<style scoped>
.canvas-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

canvas {
  position: absolute;
  top: 0;
  left: 0;
}
</style>
