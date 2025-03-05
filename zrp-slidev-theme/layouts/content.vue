<script setup lang="ts">
import Bird from '../components/bird/Bird.vue'

withDefaults(defineProps<{
  displayPageNumber?: boolean
  subject?: string
}>(), {
  displayPageNumber: true,
})
</script>

<template>
  <div class="slidev-layout content">
    <div class="relative h-full w-full flex-col flex justify-start items-left">
      <h1 v-if="subject">{{ subject }}</h1>
      <hr v-if="subject" class="w-[64px] border-1 border-dashed mb-xl border-primary">
      <slot></slot>
      <Bird class="absolute bottom-0 right-0" color="white"/>
      <span v-if="displayPageNumber" class="absolute bottom-0 left-0 text-center text-md">{{ $nav.currentPage }}</span>
    </div>
  </div>
</template>

<style>
.slidev-layout.content {
  @apply h-full grid pt-xs;

  h1 {
    @apply text-4xl mt-xs mb-sm font-bold;
    text-align: left;
    line-height: 2.5rem;
  }
}
</style>
