<script setup lang="ts">
import Bird from '../components/bird/Bird.vue';

withDefaults(
  defineProps<{
    showDate?: boolean;
  }>(), {
    showDate: true
  }
);
</script>

<template>
  <div class="slidev-layout cover">
    <div class="relative h-full w-full flex-col flex justify-center items-center">
      <slot></slot>
      <span v-if="showDate" class="absolute bottom-0 w-full text-center text-md">{{ new Date().toLocaleDateString('pt-BR') }}</span>
      <Bird class="absolute bottom-0 right-0" color="white"/>
    </div>
  </div>
</template>
