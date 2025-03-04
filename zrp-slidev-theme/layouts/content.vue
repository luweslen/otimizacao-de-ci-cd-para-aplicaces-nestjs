<script setup lang="ts">
import Bird from '../components/bird/Bird.vue';

withDefaults(defineProps<{
  displayPageNumber?: boolean
}>(), {
  displayPageNumber: true
})
</script>

<template>
  <div class="slidev-layout content">
    <div class="relative h-full w-full flex-col flex justify-start items-left">
      <slot></slot>
      <Bird class="absolute bottom-0 right-0" color="white"/>
      <span v-if="displayPageNumber" class="absolute bottom-0 left-0 text-center text-md">{{ $nav.currentPage }}</span>
    </div>
  </div>
</template>
