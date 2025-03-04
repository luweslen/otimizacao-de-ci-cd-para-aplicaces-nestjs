<script setup lang="ts">
import Bird from '../components/bird/Bird.vue';
</script>

<template>
  <div class="slidev-layout content">
    <div class="relative h-full w-full flex-col flex justify-start items-left">
      <slot></slot>
      <Bird class="absolute bottom-0 right-0" color="white"/>
    </div>
  </div>
</template>
