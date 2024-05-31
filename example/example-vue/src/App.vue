<script setup lang="ts">
import { ref } from 'vue';
import { VueMouseZoom } from 'vue-mouse-zoom';
const zoom = ref(1);
const onZoomUpdate = (scale: number) => {
  // console.log(scale);
  // zoom.value = scale;
};
</script>

<template>
  <div style="width: 300px; height: 300px; background-color: blanchedalmond">
    <VueMouseZoom
      :zoom="0.4"
      :is-draggable="true"
      @onZoomUpdate="onZoomUpdate"
    >
      <img
        src="https://avatars.githubusercontent.com/u/68246760?v=4"
        style="width: 30px; height: 200px"
      />
    </VueMouseZoom>
  </div>
</template>

<style scoped></style>
