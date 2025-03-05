<template>
  <div class="slidev-layout section py-none my-none">
    <div class="clip-parallelogram"></div>
    <hr class="absolute top-60 right-100 h-px w-[174px] my-8 border-dashed border-gray-600">
    <div class="relative h-full w-full flex-col flex justify-center items-left">
      <slot></slot>
    </div>
  </div>
</template>

<style>
.slidev-layout.section {
  @apply h-full grid pt-xs;

  .clip-parallelogram {
    @apply absolute top-0 left-0 w-2/3 h-full;
    clip-path: polygon(0 0, 100% 0%, 40% 100%, 0% 100%);
    background: var(--slidev-theme-primary);
  }

  h1 {
    @apply text-5xl font-bold;
    color: var(--zrp-background);
  }
}
</style>
