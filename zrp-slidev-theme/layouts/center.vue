<template>
  <div class="slidev-layout center">
    <div class="relative h-full w-full flex-col flex justify-center items-center">
      <slot></slot>
    </div>
  </div>
</template>

<style>
.slidev-layout.center {
  @apply h-full grid pt-xs;

  h1 {
    @apply text-6xl font-bold text-center;
  }
}
</style>
