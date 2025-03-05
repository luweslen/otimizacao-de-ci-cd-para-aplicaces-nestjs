<script setup lang="ts">
import Bird from '../components/bird/Bird.vue';

withDefaults(
  defineProps<{
    showDate?: boolean;
  }>(), {
    showDate: true,
  },
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

<style>
.slidev-layout.cover {
  @apply h-full grid;

  h1 {
    @apply text-6xl leading-20 font-bold;
    text-align: center;

    .primary:hover {
      color: var(--zrp-primary);
      transition: 0.3s;
    }

    .secondary:hover {
      color: var(--zrp-secondary);
      transition: 0.3s;
    }

    .tertiary:hover {
      color: var(--zrp-tertiary);
      transition: 0.3s;
    }
  }
}
</style>
