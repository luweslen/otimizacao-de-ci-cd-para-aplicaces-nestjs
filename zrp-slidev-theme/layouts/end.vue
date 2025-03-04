<script setup lang="ts">
import Bird from '../components/bird/Bird.vue';

const props = defineProps<{
  email?: string;
  website?: string;
}>()
</script>

<template>
  <div class="slidev-layout end">
    <div class="relative h-full w-full flex-col flex justify-center items-end">
      <Bird color="white"/>
      <div class="flex-col min-w-md max-w-xl">
        <hr class="h-px w-full my-8 bg-white border-0">
        <slot />
        <hr class="h-px w-full my-8 bg-white border-0">
      </div>
      <div class="flex flex-col items-end">
        <a :href="props.website" target="_blank">{{ props.website }}</a>
        <a :href="`mailto:${props.email}`" target="_blank">{{ props.email }}</a>
      </div>
    </div>
  </div>
</template>
